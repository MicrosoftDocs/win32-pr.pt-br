---
title: Reps-To atributo
description: Lista os servidores que o diretório notificará sobre alterações e servidores para os quais o diretório enviará alterações na solicitação para o contexto de nomenclatura definido.
ms.assetid: d7fd5a57-a0e1-4c69-9b9a-1cdad87610b1
ms.tgt_platform: multiple
keywords:
- Esquema de Reps-To do atributo AD
- Esquema de AD do atributo repsto
topic_type:
- apiref
api_name:
- Reps-To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd5c39d19eb12bb801d7ca7fb9b22ed665d59d10
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103919569"
---
# <a name="reps-to-attribute"></a><span data-ttu-id="5c221-105">Reps-To atributo</span><span class="sxs-lookup"><span data-stu-id="5c221-105">Reps-To attribute</span></span>

<span data-ttu-id="5c221-106">Lista os servidores que o diretório notificará sobre alterações e servidores para os quais o diretório enviará alterações na solicitação para o contexto de nomenclatura definido.</span><span class="sxs-lookup"><span data-stu-id="5c221-106">Lists the servers that the directory will notify of changes and servers to which the directory will send changes on Request for the defined naming context.</span></span>



| <span data-ttu-id="5c221-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="5c221-107">Entry</span></span> | <span data-ttu-id="5c221-108">Valor</span><span class="sxs-lookup"><span data-stu-id="5c221-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="5c221-109">CN</span><span class="sxs-lookup"><span data-stu-id="5c221-109">CN</span></span>                | <span data-ttu-id="5c221-110">Reps-To</span><span class="sxs-lookup"><span data-stu-id="5c221-110">Reps-To</span></span>                                               |
| <span data-ttu-id="5c221-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="5c221-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5c221-112">repsto</span><span class="sxs-lookup"><span data-stu-id="5c221-112">repsTo</span></span>                                                |
| <span data-ttu-id="5c221-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="5c221-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="5c221-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="5c221-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="5c221-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="5c221-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="5c221-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5c221-116">Attribute-Id</span></span>      | <span data-ttu-id="5c221-117">1.2.840.113556.1.2.83</span><span class="sxs-lookup"><span data-stu-id="5c221-117">1.2.840.113556.1.2.83</span></span>                                 |
| <span data-ttu-id="5c221-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5c221-118">System-Id-Guid</span></span>    | <span data-ttu-id="5c221-119">bf967a1e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="5c221-119">bf967a1e-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="5c221-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c221-120">Syntax</span></span>            | [<span data-ttu-id="5c221-121">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="5c221-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="5c221-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="5c221-122">Implementations</span></span>

-   [<span data-ttu-id="5c221-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5c221-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5c221-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5c221-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5c221-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="5c221-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="5c221-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5c221-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5c221-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5c221-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5c221-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5c221-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5c221-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5c221-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5c221-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5c221-130">Windows 2000 Server</span></span>



| <span data-ttu-id="5c221-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="5c221-131">Entry</span></span> | <span data-ttu-id="5c221-132">Valor</span><span class="sxs-lookup"><span data-stu-id="5c221-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="5c221-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="5c221-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="5c221-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c221-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="5c221-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c221-135">System-Only</span></span>            | <span data-ttu-id="5c221-136">True</span><span class="sxs-lookup"><span data-stu-id="5c221-136">True</span></span>                            |
| <span data-ttu-id="5c221-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5c221-137">Is-Single-Valued</span></span>       | <span data-ttu-id="5c221-138">Falso</span><span class="sxs-lookup"><span data-stu-id="5c221-138">False</span></span>                           |
| <span data-ttu-id="5c221-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="5c221-139">Is Indexed</span></span>             | <span data-ttu-id="5c221-140">Falso</span><span class="sxs-lookup"><span data-stu-id="5c221-140">False</span></span>                           |
| <span data-ttu-id="5c221-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5c221-141">In Global Catalog</span></span>      | <span data-ttu-id="5c221-142">True</span><span class="sxs-lookup"><span data-stu-id="5c221-142">True</span></span>                            |
| <span data-ttu-id="5c221-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5c221-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c221-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5c221-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="5c221-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c221-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="5c221-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c221-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="5c221-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c221-147">Search-Flags</span></span>           | <span data-ttu-id="5c221-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c221-148">0x00000000</span></span>                      |
| <span data-ttu-id="5c221-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c221-149">System-Flags</span></span>           | <span data-ttu-id="5c221-150">0x00000013</span><span class="sxs-lookup"><span data-stu-id="5c221-150">0x00000013</span></span>                      |
| <span data-ttu-id="5c221-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5c221-151">Classes used in</span></span>        | [<span data-ttu-id="5c221-152">**Início**</span><span class="sxs-lookup"><span data-stu-id="5c221-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5c221-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5c221-153">Windows Server 2003</span></span>



| <span data-ttu-id="5c221-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="5c221-154">Entry</span></span> | <span data-ttu-id="5c221-155">Valor</span><span class="sxs-lookup"><span data-stu-id="5c221-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="5c221-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="5c221-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="5c221-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c221-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="5c221-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c221-158">System-Only</span></span>            | <span data-ttu-id="5c221-159">True</span><span class="sxs-lookup"><span data-stu-id="5c221-159">True</span></span>                            |
| <span data-ttu-id="5c221-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5c221-160">Is-Single-Valued</span></span>       | <span data-ttu-id="5c221-161">Falso</span><span class="sxs-lookup"><span data-stu-id="5c221-161">False</span></span>                           |
| <span data-ttu-id="5c221-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="5c221-162">Is Indexed</span></span>             | <span data-ttu-id="5c221-163">Falso</span><span class="sxs-lookup"><span data-stu-id="5c221-163">False</span></span>                           |
| <span data-ttu-id="5c221-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5c221-164">In Global Catalog</span></span>      | <span data-ttu-id="5c221-165">True</span><span class="sxs-lookup"><span data-stu-id="5c221-165">True</span></span>                            |
| <span data-ttu-id="5c221-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5c221-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c221-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5c221-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="5c221-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c221-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="5c221-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c221-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="5c221-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c221-170">Search-Flags</span></span>           | <span data-ttu-id="5c221-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c221-171">0x00000000</span></span>                      |
| <span data-ttu-id="5c221-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c221-172">System-Flags</span></span>           | <span data-ttu-id="5c221-173">0x00000013</span><span class="sxs-lookup"><span data-stu-id="5c221-173">0x00000013</span></span>                      |
| <span data-ttu-id="5c221-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5c221-174">Classes used in</span></span>        | [<span data-ttu-id="5c221-175">**Início**</span><span class="sxs-lookup"><span data-stu-id="5c221-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="5c221-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="5c221-176">ADAM</span></span>



| <span data-ttu-id="5c221-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="5c221-177">Entry</span></span> | <span data-ttu-id="5c221-178">Valor</span><span class="sxs-lookup"><span data-stu-id="5c221-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="5c221-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="5c221-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="5c221-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c221-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="5c221-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c221-181">System-Only</span></span>            | <span data-ttu-id="5c221-182">True</span><span class="sxs-lookup"><span data-stu-id="5c221-182">True</span></span>                            |
| <span data-ttu-id="5c221-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5c221-183">Is-Single-Valued</span></span>       | <span data-ttu-id="5c221-184">Falso</span><span class="sxs-lookup"><span data-stu-id="5c221-184">False</span></span>                           |
| <span data-ttu-id="5c221-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="5c221-185">Is Indexed</span></span>             | <span data-ttu-id="5c221-186">Falso</span><span class="sxs-lookup"><span data-stu-id="5c221-186">False</span></span>                           |
| <span data-ttu-id="5c221-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5c221-187">In Global Catalog</span></span>      | <span data-ttu-id="5c221-188">True</span><span class="sxs-lookup"><span data-stu-id="5c221-188">True</span></span>                            |
| <span data-ttu-id="5c221-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5c221-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c221-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5c221-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="5c221-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c221-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="5c221-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c221-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="5c221-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c221-193">Search-Flags</span></span>           | <span data-ttu-id="5c221-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c221-194">0x00000000</span></span>                      |
| <span data-ttu-id="5c221-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c221-195">System-Flags</span></span>           | <span data-ttu-id="5c221-196">0x00000013</span><span class="sxs-lookup"><span data-stu-id="5c221-196">0x00000013</span></span>                      |
| <span data-ttu-id="5c221-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5c221-197">Classes used in</span></span>        | [<span data-ttu-id="5c221-198">**Início**</span><span class="sxs-lookup"><span data-stu-id="5c221-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5c221-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5c221-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5c221-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="5c221-200">Entry</span></span> | <span data-ttu-id="5c221-201">Valor</span><span class="sxs-lookup"><span data-stu-id="5c221-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="5c221-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="5c221-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="5c221-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c221-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="5c221-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c221-204">System-Only</span></span>            | <span data-ttu-id="5c221-205">True</span><span class="sxs-lookup"><span data-stu-id="5c221-205">True</span></span>                            |
| <span data-ttu-id="5c221-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5c221-206">Is-Single-Valued</span></span>       | <span data-ttu-id="5c221-207">Falso</span><span class="sxs-lookup"><span data-stu-id="5c221-207">False</span></span>                           |
| <span data-ttu-id="5c221-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="5c221-208">Is Indexed</span></span>             | <span data-ttu-id="5c221-209">Falso</span><span class="sxs-lookup"><span data-stu-id="5c221-209">False</span></span>                           |
| <span data-ttu-id="5c221-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5c221-210">In Global Catalog</span></span>      | <span data-ttu-id="5c221-211">True</span><span class="sxs-lookup"><span data-stu-id="5c221-211">True</span></span>                            |
| <span data-ttu-id="5c221-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5c221-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c221-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5c221-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="5c221-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c221-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="5c221-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c221-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="5c221-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c221-216">Search-Flags</span></span>           | <span data-ttu-id="5c221-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c221-217">0x00000000</span></span>                      |
| <span data-ttu-id="5c221-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c221-218">System-Flags</span></span>           | <span data-ttu-id="5c221-219">0x00000013</span><span class="sxs-lookup"><span data-stu-id="5c221-219">0x00000013</span></span>                      |
| <span data-ttu-id="5c221-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5c221-220">Classes used in</span></span>        | [<span data-ttu-id="5c221-221">**Início**</span><span class="sxs-lookup"><span data-stu-id="5c221-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5c221-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c221-222">Windows Server 2008</span></span>



| <span data-ttu-id="5c221-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="5c221-223">Entry</span></span> | <span data-ttu-id="5c221-224">Valor</span><span class="sxs-lookup"><span data-stu-id="5c221-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="5c221-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="5c221-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="5c221-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c221-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="5c221-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c221-227">System-Only</span></span>            | <span data-ttu-id="5c221-228">True</span><span class="sxs-lookup"><span data-stu-id="5c221-228">True</span></span>                            |
| <span data-ttu-id="5c221-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5c221-229">Is-Single-Valued</span></span>       | <span data-ttu-id="5c221-230">Falso</span><span class="sxs-lookup"><span data-stu-id="5c221-230">False</span></span>                           |
| <span data-ttu-id="5c221-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="5c221-231">Is Indexed</span></span>             | <span data-ttu-id="5c221-232">Falso</span><span class="sxs-lookup"><span data-stu-id="5c221-232">False</span></span>                           |
| <span data-ttu-id="5c221-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5c221-233">In Global Catalog</span></span>      | <span data-ttu-id="5c221-234">True</span><span class="sxs-lookup"><span data-stu-id="5c221-234">True</span></span>                            |
| <span data-ttu-id="5c221-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5c221-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c221-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5c221-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="5c221-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c221-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="5c221-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c221-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="5c221-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c221-239">Search-Flags</span></span>           | <span data-ttu-id="5c221-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c221-240">0x00000000</span></span>                      |
| <span data-ttu-id="5c221-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c221-241">System-Flags</span></span>           | <span data-ttu-id="5c221-242">0x00000013</span><span class="sxs-lookup"><span data-stu-id="5c221-242">0x00000013</span></span>                      |
| <span data-ttu-id="5c221-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5c221-243">Classes used in</span></span>        | [<span data-ttu-id="5c221-244">**Início**</span><span class="sxs-lookup"><span data-stu-id="5c221-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5c221-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5c221-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5c221-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="5c221-246">Entry</span></span> | <span data-ttu-id="5c221-247">Valor</span><span class="sxs-lookup"><span data-stu-id="5c221-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="5c221-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="5c221-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="5c221-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c221-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="5c221-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c221-250">System-Only</span></span>            | <span data-ttu-id="5c221-251">True</span><span class="sxs-lookup"><span data-stu-id="5c221-251">True</span></span>                            |
| <span data-ttu-id="5c221-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5c221-252">Is-Single-Valued</span></span>       | <span data-ttu-id="5c221-253">Falso</span><span class="sxs-lookup"><span data-stu-id="5c221-253">False</span></span>                           |
| <span data-ttu-id="5c221-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="5c221-254">Is Indexed</span></span>             | <span data-ttu-id="5c221-255">Falso</span><span class="sxs-lookup"><span data-stu-id="5c221-255">False</span></span>                           |
| <span data-ttu-id="5c221-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5c221-256">In Global Catalog</span></span>      | <span data-ttu-id="5c221-257">True</span><span class="sxs-lookup"><span data-stu-id="5c221-257">True</span></span>                            |
| <span data-ttu-id="5c221-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5c221-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c221-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5c221-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="5c221-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c221-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="5c221-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c221-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="5c221-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c221-262">Search-Flags</span></span>           | <span data-ttu-id="5c221-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c221-263">0x00000000</span></span>                      |
| <span data-ttu-id="5c221-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c221-264">System-Flags</span></span>           | <span data-ttu-id="5c221-265">0x00000013</span><span class="sxs-lookup"><span data-stu-id="5c221-265">0x00000013</span></span>                      |
| <span data-ttu-id="5c221-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5c221-266">Classes used in</span></span>        | [<span data-ttu-id="5c221-267">**Início**</span><span class="sxs-lookup"><span data-stu-id="5c221-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5c221-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5c221-268">Windows Server 2012</span></span>



| <span data-ttu-id="5c221-269">Entrada</span><span class="sxs-lookup"><span data-stu-id="5c221-269">Entry</span></span> | <span data-ttu-id="5c221-270">Valor</span><span class="sxs-lookup"><span data-stu-id="5c221-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="5c221-271">ID do link</span><span class="sxs-lookup"><span data-stu-id="5c221-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="5c221-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c221-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="5c221-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c221-273">System-Only</span></span>            | <span data-ttu-id="5c221-274">True</span><span class="sxs-lookup"><span data-stu-id="5c221-274">True</span></span>                            |
| <span data-ttu-id="5c221-275">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5c221-275">Is-Single-Valued</span></span>       | <span data-ttu-id="5c221-276">Falso</span><span class="sxs-lookup"><span data-stu-id="5c221-276">False</span></span>                           |
| <span data-ttu-id="5c221-277">É indexado</span><span class="sxs-lookup"><span data-stu-id="5c221-277">Is Indexed</span></span>             | <span data-ttu-id="5c221-278">Falso</span><span class="sxs-lookup"><span data-stu-id="5c221-278">False</span></span>                           |
| <span data-ttu-id="5c221-279">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5c221-279">In Global Catalog</span></span>      | <span data-ttu-id="5c221-280">True</span><span class="sxs-lookup"><span data-stu-id="5c221-280">True</span></span>                            |
| <span data-ttu-id="5c221-281">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5c221-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c221-282">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5c221-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="5c221-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c221-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="5c221-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c221-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="5c221-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c221-285">Search-Flags</span></span>           | <span data-ttu-id="5c221-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c221-286">0x00000000</span></span>                      |
| <span data-ttu-id="5c221-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c221-287">System-Flags</span></span>           | <span data-ttu-id="5c221-288">0x00000013</span><span class="sxs-lookup"><span data-stu-id="5c221-288">0x00000013</span></span>                      |
| <span data-ttu-id="5c221-289">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5c221-289">Classes used in</span></span>        | [<span data-ttu-id="5c221-290">**Início**</span><span class="sxs-lookup"><span data-stu-id="5c221-290">**Top**</span></span>](c-top.md)<br/> |



 

 





