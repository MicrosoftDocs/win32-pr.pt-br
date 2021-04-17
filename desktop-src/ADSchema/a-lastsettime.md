---
title: Último-conjunto-atributo de tempo
description: A última vez em que o segredo foi alterado.
ms.assetid: 71245cd4-90d8-4aa1-ad96-d46d6b3a7ad0
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo de tempo Last-set-time
- Esquema de AD do atributo lastSetTime
topic_type:
- apiref
api_name:
- Last-Set-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce123377fac6e67de1ba84b906c9498d0a064936
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104369994"
---
# <a name="last-set-time-attribute"></a><span data-ttu-id="9187d-105">Último-conjunto-atributo de tempo</span><span class="sxs-lookup"><span data-stu-id="9187d-105">Last-Set-Time attribute</span></span>

<span data-ttu-id="9187d-106">A última vez em que o segredo foi alterado.</span><span class="sxs-lookup"><span data-stu-id="9187d-106">The last time the secret was changed.</span></span> <span data-ttu-id="9187d-107">Esse valor é armazenado como um inteiro grande que representa o número de intervalos de 100 a nanossegundos desde 1º de janeiro de 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="9187d-107">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span>



| <span data-ttu-id="9187d-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="9187d-108">Entry</span></span> | <span data-ttu-id="9187d-109">Valor</span><span class="sxs-lookup"><span data-stu-id="9187d-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="9187d-110">CN</span><span class="sxs-lookup"><span data-stu-id="9187d-110">CN</span></span>                | <span data-ttu-id="9187d-111">Hora do último conjunto</span><span class="sxs-lookup"><span data-stu-id="9187d-111">Last-Set-Time</span></span>                        |
| <span data-ttu-id="9187d-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9187d-112">Ldap-Display-Name</span></span> | <span data-ttu-id="9187d-113">lastSetTime</span><span class="sxs-lookup"><span data-stu-id="9187d-113">lastSetTime</span></span>                          |
| <span data-ttu-id="9187d-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="9187d-114">Size</span></span>              | <span data-ttu-id="9187d-115">8 bytes</span><span class="sxs-lookup"><span data-stu-id="9187d-115">8 bytes</span></span>                              |
| <span data-ttu-id="9187d-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="9187d-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="9187d-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="9187d-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="9187d-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9187d-118">Attribute-Id</span></span>      | <span data-ttu-id="9187d-119">1.2.840.113556.1.4.53</span><span class="sxs-lookup"><span data-stu-id="9187d-119">1.2.840.113556.1.4.53</span></span>                |
| <span data-ttu-id="9187d-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9187d-120">System-Id-Guid</span></span>    | <span data-ttu-id="9187d-121">bf967998-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="9187d-121">bf967998-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="9187d-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="9187d-122">Syntax</span></span>            | [<span data-ttu-id="9187d-123">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="9187d-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="9187d-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="9187d-124">Implementations</span></span>

-   [<span data-ttu-id="9187d-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9187d-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9187d-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9187d-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9187d-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9187d-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9187d-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9187d-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9187d-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9187d-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9187d-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9187d-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9187d-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9187d-131">Windows 2000 Server</span></span>



| <span data-ttu-id="9187d-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="9187d-132">Entry</span></span> | <span data-ttu-id="9187d-133">Valor</span><span class="sxs-lookup"><span data-stu-id="9187d-133">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="9187d-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="9187d-134">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="9187d-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9187d-135">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="9187d-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="9187d-136">System-Only</span></span>            | <span data-ttu-id="9187d-137">Falso</span><span class="sxs-lookup"><span data-stu-id="9187d-137">False</span></span>                                 |
| <span data-ttu-id="9187d-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9187d-138">Is-Single-Valued</span></span>       | <span data-ttu-id="9187d-139">True</span><span class="sxs-lookup"><span data-stu-id="9187d-139">True</span></span>                                  |
| <span data-ttu-id="9187d-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="9187d-140">Is Indexed</span></span>             | <span data-ttu-id="9187d-141">Falso</span><span class="sxs-lookup"><span data-stu-id="9187d-141">False</span></span>                                 |
| <span data-ttu-id="9187d-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9187d-142">In Global Catalog</span></span>      | <span data-ttu-id="9187d-143">Falso</span><span class="sxs-lookup"><span data-stu-id="9187d-143">False</span></span>                                 |
| <span data-ttu-id="9187d-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9187d-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="9187d-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9187d-145">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="9187d-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9187d-146">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="9187d-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9187d-147">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="9187d-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9187d-148">Search-Flags</span></span>           | <span data-ttu-id="9187d-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9187d-149">0x00000000</span></span>                            |
| <span data-ttu-id="9187d-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9187d-150">System-Flags</span></span>           | <span data-ttu-id="9187d-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9187d-151">0x00000010</span></span>                            |
| <span data-ttu-id="9187d-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9187d-152">Classes used in</span></span>        | [<span data-ttu-id="9187d-153">**RADIUS**</span><span class="sxs-lookup"><span data-stu-id="9187d-153">**Secret**</span></span>](c-secret.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9187d-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9187d-154">Windows Server 2003</span></span>



| <span data-ttu-id="9187d-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="9187d-155">Entry</span></span> | <span data-ttu-id="9187d-156">Valor</span><span class="sxs-lookup"><span data-stu-id="9187d-156">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="9187d-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="9187d-157">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="9187d-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9187d-158">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="9187d-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="9187d-159">System-Only</span></span>            | <span data-ttu-id="9187d-160">Falso</span><span class="sxs-lookup"><span data-stu-id="9187d-160">False</span></span>                                 |
| <span data-ttu-id="9187d-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9187d-161">Is-Single-Valued</span></span>       | <span data-ttu-id="9187d-162">True</span><span class="sxs-lookup"><span data-stu-id="9187d-162">True</span></span>                                  |
| <span data-ttu-id="9187d-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="9187d-163">Is Indexed</span></span>             | <span data-ttu-id="9187d-164">Falso</span><span class="sxs-lookup"><span data-stu-id="9187d-164">False</span></span>                                 |
| <span data-ttu-id="9187d-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9187d-165">In Global Catalog</span></span>      | <span data-ttu-id="9187d-166">Falso</span><span class="sxs-lookup"><span data-stu-id="9187d-166">False</span></span>                                 |
| <span data-ttu-id="9187d-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9187d-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="9187d-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9187d-168">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="9187d-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9187d-169">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="9187d-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9187d-170">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="9187d-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9187d-171">Search-Flags</span></span>           | <span data-ttu-id="9187d-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9187d-172">0x00000000</span></span>                            |
| <span data-ttu-id="9187d-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9187d-173">System-Flags</span></span>           | <span data-ttu-id="9187d-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9187d-174">0x00000010</span></span>                            |
| <span data-ttu-id="9187d-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9187d-175">Classes used in</span></span>        | [<span data-ttu-id="9187d-176">**RADIUS**</span><span class="sxs-lookup"><span data-stu-id="9187d-176">**Secret**</span></span>](c-secret.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9187d-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9187d-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9187d-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="9187d-178">Entry</span></span> | <span data-ttu-id="9187d-179">Valor</span><span class="sxs-lookup"><span data-stu-id="9187d-179">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="9187d-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="9187d-180">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="9187d-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9187d-181">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="9187d-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="9187d-182">System-Only</span></span>            | <span data-ttu-id="9187d-183">Falso</span><span class="sxs-lookup"><span data-stu-id="9187d-183">False</span></span>                                 |
| <span data-ttu-id="9187d-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9187d-184">Is-Single-Valued</span></span>       | <span data-ttu-id="9187d-185">True</span><span class="sxs-lookup"><span data-stu-id="9187d-185">True</span></span>                                  |
| <span data-ttu-id="9187d-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="9187d-186">Is Indexed</span></span>             | <span data-ttu-id="9187d-187">Falso</span><span class="sxs-lookup"><span data-stu-id="9187d-187">False</span></span>                                 |
| <span data-ttu-id="9187d-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9187d-188">In Global Catalog</span></span>      | <span data-ttu-id="9187d-189">Falso</span><span class="sxs-lookup"><span data-stu-id="9187d-189">False</span></span>                                 |
| <span data-ttu-id="9187d-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9187d-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="9187d-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9187d-191">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="9187d-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9187d-192">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="9187d-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9187d-193">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="9187d-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9187d-194">Search-Flags</span></span>           | <span data-ttu-id="9187d-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9187d-195">0x00000000</span></span>                            |
| <span data-ttu-id="9187d-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9187d-196">System-Flags</span></span>           | <span data-ttu-id="9187d-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9187d-197">0x00000010</span></span>                            |
| <span data-ttu-id="9187d-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9187d-198">Classes used in</span></span>        | [<span data-ttu-id="9187d-199">**RADIUS**</span><span class="sxs-lookup"><span data-stu-id="9187d-199">**Secret**</span></span>](c-secret.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9187d-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9187d-200">Windows Server 2008</span></span>



| <span data-ttu-id="9187d-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="9187d-201">Entry</span></span> | <span data-ttu-id="9187d-202">Valor</span><span class="sxs-lookup"><span data-stu-id="9187d-202">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="9187d-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="9187d-203">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="9187d-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9187d-204">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="9187d-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="9187d-205">System-Only</span></span>            | <span data-ttu-id="9187d-206">Falso</span><span class="sxs-lookup"><span data-stu-id="9187d-206">False</span></span>                                 |
| <span data-ttu-id="9187d-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9187d-207">Is-Single-Valued</span></span>       | <span data-ttu-id="9187d-208">True</span><span class="sxs-lookup"><span data-stu-id="9187d-208">True</span></span>                                  |
| <span data-ttu-id="9187d-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="9187d-209">Is Indexed</span></span>             | <span data-ttu-id="9187d-210">Falso</span><span class="sxs-lookup"><span data-stu-id="9187d-210">False</span></span>                                 |
| <span data-ttu-id="9187d-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9187d-211">In Global Catalog</span></span>      | <span data-ttu-id="9187d-212">Falso</span><span class="sxs-lookup"><span data-stu-id="9187d-212">False</span></span>                                 |
| <span data-ttu-id="9187d-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9187d-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="9187d-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9187d-214">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="9187d-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9187d-215">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="9187d-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9187d-216">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="9187d-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9187d-217">Search-Flags</span></span>           | <span data-ttu-id="9187d-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9187d-218">0x00000000</span></span>                            |
| <span data-ttu-id="9187d-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9187d-219">System-Flags</span></span>           | <span data-ttu-id="9187d-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9187d-220">0x00000010</span></span>                            |
| <span data-ttu-id="9187d-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9187d-221">Classes used in</span></span>        | [<span data-ttu-id="9187d-222">**RADIUS**</span><span class="sxs-lookup"><span data-stu-id="9187d-222">**Secret**</span></span>](c-secret.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9187d-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9187d-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9187d-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="9187d-224">Entry</span></span> | <span data-ttu-id="9187d-225">Valor</span><span class="sxs-lookup"><span data-stu-id="9187d-225">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="9187d-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="9187d-226">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="9187d-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9187d-227">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="9187d-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="9187d-228">System-Only</span></span>            | <span data-ttu-id="9187d-229">Falso</span><span class="sxs-lookup"><span data-stu-id="9187d-229">False</span></span>                                 |
| <span data-ttu-id="9187d-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9187d-230">Is-Single-Valued</span></span>       | <span data-ttu-id="9187d-231">True</span><span class="sxs-lookup"><span data-stu-id="9187d-231">True</span></span>                                  |
| <span data-ttu-id="9187d-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="9187d-232">Is Indexed</span></span>             | <span data-ttu-id="9187d-233">Falso</span><span class="sxs-lookup"><span data-stu-id="9187d-233">False</span></span>                                 |
| <span data-ttu-id="9187d-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9187d-234">In Global Catalog</span></span>      | <span data-ttu-id="9187d-235">Falso</span><span class="sxs-lookup"><span data-stu-id="9187d-235">False</span></span>                                 |
| <span data-ttu-id="9187d-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9187d-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="9187d-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9187d-237">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="9187d-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9187d-238">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="9187d-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9187d-239">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="9187d-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9187d-240">Search-Flags</span></span>           | <span data-ttu-id="9187d-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9187d-241">0x00000000</span></span>                            |
| <span data-ttu-id="9187d-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9187d-242">System-Flags</span></span>           | <span data-ttu-id="9187d-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9187d-243">0x00000010</span></span>                            |
| <span data-ttu-id="9187d-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9187d-244">Classes used in</span></span>        | [<span data-ttu-id="9187d-245">**RADIUS**</span><span class="sxs-lookup"><span data-stu-id="9187d-245">**Secret**</span></span>](c-secret.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9187d-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9187d-246">Windows Server 2012</span></span>



| <span data-ttu-id="9187d-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="9187d-247">Entry</span></span> | <span data-ttu-id="9187d-248">Valor</span><span class="sxs-lookup"><span data-stu-id="9187d-248">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="9187d-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="9187d-249">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="9187d-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9187d-250">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="9187d-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="9187d-251">System-Only</span></span>            | <span data-ttu-id="9187d-252">Falso</span><span class="sxs-lookup"><span data-stu-id="9187d-252">False</span></span>                                 |
| <span data-ttu-id="9187d-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9187d-253">Is-Single-Valued</span></span>       | <span data-ttu-id="9187d-254">True</span><span class="sxs-lookup"><span data-stu-id="9187d-254">True</span></span>                                  |
| <span data-ttu-id="9187d-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="9187d-255">Is Indexed</span></span>             | <span data-ttu-id="9187d-256">Falso</span><span class="sxs-lookup"><span data-stu-id="9187d-256">False</span></span>                                 |
| <span data-ttu-id="9187d-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9187d-257">In Global Catalog</span></span>      | <span data-ttu-id="9187d-258">Falso</span><span class="sxs-lookup"><span data-stu-id="9187d-258">False</span></span>                                 |
| <span data-ttu-id="9187d-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9187d-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="9187d-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9187d-260">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="9187d-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9187d-261">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="9187d-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9187d-262">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="9187d-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9187d-263">Search-Flags</span></span>           | <span data-ttu-id="9187d-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9187d-264">0x00000000</span></span>                            |
| <span data-ttu-id="9187d-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9187d-265">System-Flags</span></span>           | <span data-ttu-id="9187d-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9187d-266">0x00000010</span></span>                            |
| <span data-ttu-id="9187d-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9187d-267">Classes used in</span></span>        | [<span data-ttu-id="9187d-268">**RADIUS**</span><span class="sxs-lookup"><span data-stu-id="9187d-268">**Secret**</span></span>](c-secret.md)<br/> |



 

 





