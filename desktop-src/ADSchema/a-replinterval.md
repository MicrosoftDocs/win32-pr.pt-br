---
title: Repl-Interval atributo
description: O atributo de objetos Site-Link que define o intervalo, em minutos, entre os ciclos de replicação entre os sites na lista de sites.
ms.assetid: ef4cbf75-7283-4930-9f98-1ffd6eb05669
ms.tgt_platform: multiple
keywords:
- Esquema de Repl-Interval do atributo AD
- Esquema de AD do atributo replInterval
topic_type:
- apiref
api_name:
- Repl-Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e681b01fbc60b775b0cb947007056dc1d3d3adbb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086859"
---
# <a name="repl-interval-attribute"></a><span data-ttu-id="bf64a-105">Repl-Interval atributo</span><span class="sxs-lookup"><span data-stu-id="bf64a-105">Repl-Interval attribute</span></span>

<span data-ttu-id="bf64a-106">O atributo de objetos Site-Link que define o intervalo, em minutos, entre os ciclos de replicação entre os sites na lista de sites.</span><span class="sxs-lookup"><span data-stu-id="bf64a-106">The attribute of Site-Link objects that defines the interval, in minutes, between replication cycles between the sites in the Site-List.</span></span> <span data-ttu-id="bf64a-107">Deve ser um múltiplo de 15 minutos (a granularidade da replicação de DS entre sites), um mínimo de 15 minutos e um máximo de 10.080 minutos (uma semana).</span><span class="sxs-lookup"><span data-stu-id="bf64a-107">Must be a multiple of 15 minutes (the granularity of cross-site DS replication), a minimum of 15 minutes, and a maximum of 10,080 minutes (one week).</span></span>



| <span data-ttu-id="bf64a-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="bf64a-108">Entry</span></span> | <span data-ttu-id="bf64a-109">Valor</span><span class="sxs-lookup"><span data-stu-id="bf64a-109">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="bf64a-110">CN</span><span class="sxs-lookup"><span data-stu-id="bf64a-110">CN</span></span>                | <span data-ttu-id="bf64a-111">Repl-Interval</span><span class="sxs-lookup"><span data-stu-id="bf64a-111">Repl-Interval</span></span>                                  |
| <span data-ttu-id="bf64a-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="bf64a-112">Ldap-Display-Name</span></span> | <span data-ttu-id="bf64a-113">replInterval</span><span class="sxs-lookup"><span data-stu-id="bf64a-113">replInterval</span></span>                                   |
| <span data-ttu-id="bf64a-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="bf64a-114">Size</span></span>              | <span data-ttu-id="bf64a-115">4 bytes</span><span class="sxs-lookup"><span data-stu-id="bf64a-115">4 bytes</span></span>                                        |
| <span data-ttu-id="bf64a-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="bf64a-116">Update Privilege</span></span>  | <span data-ttu-id="bf64a-117">Administrador corporativo</span><span class="sxs-lookup"><span data-stu-id="bf64a-117">Enterprise administrator</span></span>                       |
| <span data-ttu-id="bf64a-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="bf64a-118">Update Frequency</span></span>  | <span data-ttu-id="bf64a-119">Quando o intervalo de replicação precisa ser alterado.</span><span class="sxs-lookup"><span data-stu-id="bf64a-119">When the replication interval needs to change.</span></span> |
| <span data-ttu-id="bf64a-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bf64a-120">Attribute-Id</span></span>      | <span data-ttu-id="bf64a-121">1.2.840.113556.1.4.1336</span><span class="sxs-lookup"><span data-stu-id="bf64a-121">1.2.840.113556.1.4.1336</span></span>                        |
| <span data-ttu-id="bf64a-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="bf64a-122">System-Id-Guid</span></span>    | <span data-ttu-id="bf64a-123">45ba9d1a-56fa-11d2-90d0-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="bf64a-123">45ba9d1a-56fa-11d2-90d0-00c04fd91ab1</span></span>           |
| <span data-ttu-id="bf64a-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf64a-124">Syntax</span></span>            | [<span data-ttu-id="bf64a-125">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="bf64a-125">**Enumeration**</span></span>](s-enumeration.md)           |



## <a name="implementations"></a><span data-ttu-id="bf64a-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="bf64a-126">Implementations</span></span>

-   [<span data-ttu-id="bf64a-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bf64a-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bf64a-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bf64a-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bf64a-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="bf64a-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="bf64a-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bf64a-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bf64a-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bf64a-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bf64a-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bf64a-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bf64a-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bf64a-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bf64a-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bf64a-134">Windows 2000 Server</span></span>



| <span data-ttu-id="bf64a-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="bf64a-135">Entry</span></span> | <span data-ttu-id="bf64a-136">Valor</span><span class="sxs-lookup"><span data-stu-id="bf64a-136">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf64a-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="bf64a-137">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="bf64a-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf64a-138">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="bf64a-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf64a-139">System-Only</span></span>            | <span data-ttu-id="bf64a-140">Falso</span><span class="sxs-lookup"><span data-stu-id="bf64a-140">False</span></span>                                                                                                      |
| <span data-ttu-id="bf64a-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bf64a-141">Is-Single-Valued</span></span>       | <span data-ttu-id="bf64a-142">True</span><span class="sxs-lookup"><span data-stu-id="bf64a-142">True</span></span>                                                                                                       |
| <span data-ttu-id="bf64a-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="bf64a-143">Is Indexed</span></span>             | <span data-ttu-id="bf64a-144">Falso</span><span class="sxs-lookup"><span data-stu-id="bf64a-144">False</span></span>                                                                                                      |
| <span data-ttu-id="bf64a-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bf64a-145">In Global Catalog</span></span>      | <span data-ttu-id="bf64a-146">Falso</span><span class="sxs-lookup"><span data-stu-id="bf64a-146">False</span></span>                                                                                                      |
| <span data-ttu-id="bf64a-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bf64a-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf64a-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bf64a-148">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="bf64a-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf64a-149">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="bf64a-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf64a-150">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="bf64a-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf64a-151">Search-Flags</span></span>           | <span data-ttu-id="bf64a-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf64a-152">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="bf64a-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf64a-153">System-Flags</span></span>           | <span data-ttu-id="bf64a-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf64a-154">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="bf64a-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bf64a-155">Classes used in</span></span>        | [<span data-ttu-id="bf64a-156">**Transporte entre sites**</span><span class="sxs-lookup"><span data-stu-id="bf64a-156">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="bf64a-157">**Link de site**</span><span class="sxs-lookup"><span data-stu-id="bf64a-157">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bf64a-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bf64a-158">Windows Server 2003</span></span>



| <span data-ttu-id="bf64a-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="bf64a-159">Entry</span></span> | <span data-ttu-id="bf64a-160">Valor</span><span class="sxs-lookup"><span data-stu-id="bf64a-160">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf64a-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="bf64a-161">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="bf64a-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf64a-162">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="bf64a-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf64a-163">System-Only</span></span>            | <span data-ttu-id="bf64a-164">Falso</span><span class="sxs-lookup"><span data-stu-id="bf64a-164">False</span></span>                                                                                                      |
| <span data-ttu-id="bf64a-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bf64a-165">Is-Single-Valued</span></span>       | <span data-ttu-id="bf64a-166">True</span><span class="sxs-lookup"><span data-stu-id="bf64a-166">True</span></span>                                                                                                       |
| <span data-ttu-id="bf64a-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="bf64a-167">Is Indexed</span></span>             | <span data-ttu-id="bf64a-168">Falso</span><span class="sxs-lookup"><span data-stu-id="bf64a-168">False</span></span>                                                                                                      |
| <span data-ttu-id="bf64a-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bf64a-169">In Global Catalog</span></span>      | <span data-ttu-id="bf64a-170">Falso</span><span class="sxs-lookup"><span data-stu-id="bf64a-170">False</span></span>                                                                                                      |
| <span data-ttu-id="bf64a-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bf64a-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf64a-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bf64a-172">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="bf64a-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf64a-173">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="bf64a-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf64a-174">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="bf64a-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf64a-175">Search-Flags</span></span>           | <span data-ttu-id="bf64a-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf64a-176">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="bf64a-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf64a-177">System-Flags</span></span>           | <span data-ttu-id="bf64a-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf64a-178">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="bf64a-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bf64a-179">Classes used in</span></span>        | [<span data-ttu-id="bf64a-180">**Transporte entre sites**</span><span class="sxs-lookup"><span data-stu-id="bf64a-180">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="bf64a-181">**Link de site**</span><span class="sxs-lookup"><span data-stu-id="bf64a-181">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="adam"></a><span data-ttu-id="bf64a-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="bf64a-182">ADAM</span></span>



| <span data-ttu-id="bf64a-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="bf64a-183">Entry</span></span> | <span data-ttu-id="bf64a-184">Valor</span><span class="sxs-lookup"><span data-stu-id="bf64a-184">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf64a-185">ID do link</span><span class="sxs-lookup"><span data-stu-id="bf64a-185">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="bf64a-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf64a-186">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="bf64a-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf64a-187">System-Only</span></span>            | <span data-ttu-id="bf64a-188">Falso</span><span class="sxs-lookup"><span data-stu-id="bf64a-188">False</span></span>                                                                                                      |
| <span data-ttu-id="bf64a-189">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bf64a-189">Is-Single-Valued</span></span>       | <span data-ttu-id="bf64a-190">True</span><span class="sxs-lookup"><span data-stu-id="bf64a-190">True</span></span>                                                                                                       |
| <span data-ttu-id="bf64a-191">É indexado</span><span class="sxs-lookup"><span data-stu-id="bf64a-191">Is Indexed</span></span>             | <span data-ttu-id="bf64a-192">Falso</span><span class="sxs-lookup"><span data-stu-id="bf64a-192">False</span></span>                                                                                                      |
| <span data-ttu-id="bf64a-193">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bf64a-193">In Global Catalog</span></span>      | <span data-ttu-id="bf64a-194">Falso</span><span class="sxs-lookup"><span data-stu-id="bf64a-194">False</span></span>                                                                                                      |
| <span data-ttu-id="bf64a-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bf64a-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf64a-196">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bf64a-196">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="bf64a-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf64a-197">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="bf64a-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf64a-198">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="bf64a-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf64a-199">Search-Flags</span></span>           | <span data-ttu-id="bf64a-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf64a-200">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="bf64a-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf64a-201">System-Flags</span></span>           | <span data-ttu-id="bf64a-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf64a-202">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="bf64a-203">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bf64a-203">Classes used in</span></span>        | [<span data-ttu-id="bf64a-204">**Transporte entre sites**</span><span class="sxs-lookup"><span data-stu-id="bf64a-204">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="bf64a-205">**Link de site**</span><span class="sxs-lookup"><span data-stu-id="bf64a-205">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bf64a-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bf64a-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bf64a-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="bf64a-207">Entry</span></span> | <span data-ttu-id="bf64a-208">Valor</span><span class="sxs-lookup"><span data-stu-id="bf64a-208">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf64a-209">ID do link</span><span class="sxs-lookup"><span data-stu-id="bf64a-209">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="bf64a-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf64a-210">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="bf64a-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf64a-211">System-Only</span></span>            | <span data-ttu-id="bf64a-212">Falso</span><span class="sxs-lookup"><span data-stu-id="bf64a-212">False</span></span>                                                                                                      |
| <span data-ttu-id="bf64a-213">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bf64a-213">Is-Single-Valued</span></span>       | <span data-ttu-id="bf64a-214">True</span><span class="sxs-lookup"><span data-stu-id="bf64a-214">True</span></span>                                                                                                       |
| <span data-ttu-id="bf64a-215">É indexado</span><span class="sxs-lookup"><span data-stu-id="bf64a-215">Is Indexed</span></span>             | <span data-ttu-id="bf64a-216">Falso</span><span class="sxs-lookup"><span data-stu-id="bf64a-216">False</span></span>                                                                                                      |
| <span data-ttu-id="bf64a-217">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bf64a-217">In Global Catalog</span></span>      | <span data-ttu-id="bf64a-218">Falso</span><span class="sxs-lookup"><span data-stu-id="bf64a-218">False</span></span>                                                                                                      |
| <span data-ttu-id="bf64a-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bf64a-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf64a-220">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bf64a-220">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="bf64a-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf64a-221">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="bf64a-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf64a-222">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="bf64a-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf64a-223">Search-Flags</span></span>           | <span data-ttu-id="bf64a-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf64a-224">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="bf64a-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf64a-225">System-Flags</span></span>           | <span data-ttu-id="bf64a-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf64a-226">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="bf64a-227">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bf64a-227">Classes used in</span></span>        | [<span data-ttu-id="bf64a-228">**Transporte entre sites**</span><span class="sxs-lookup"><span data-stu-id="bf64a-228">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="bf64a-229">**Link de site**</span><span class="sxs-lookup"><span data-stu-id="bf64a-229">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bf64a-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bf64a-230">Windows Server 2008</span></span>



| <span data-ttu-id="bf64a-231">Entrada</span><span class="sxs-lookup"><span data-stu-id="bf64a-231">Entry</span></span> | <span data-ttu-id="bf64a-232">Valor</span><span class="sxs-lookup"><span data-stu-id="bf64a-232">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf64a-233">ID do link</span><span class="sxs-lookup"><span data-stu-id="bf64a-233">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="bf64a-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf64a-234">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="bf64a-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf64a-235">System-Only</span></span>            | <span data-ttu-id="bf64a-236">Falso</span><span class="sxs-lookup"><span data-stu-id="bf64a-236">False</span></span>                                                                                                      |
| <span data-ttu-id="bf64a-237">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bf64a-237">Is-Single-Valued</span></span>       | <span data-ttu-id="bf64a-238">True</span><span class="sxs-lookup"><span data-stu-id="bf64a-238">True</span></span>                                                                                                       |
| <span data-ttu-id="bf64a-239">É indexado</span><span class="sxs-lookup"><span data-stu-id="bf64a-239">Is Indexed</span></span>             | <span data-ttu-id="bf64a-240">Falso</span><span class="sxs-lookup"><span data-stu-id="bf64a-240">False</span></span>                                                                                                      |
| <span data-ttu-id="bf64a-241">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bf64a-241">In Global Catalog</span></span>      | <span data-ttu-id="bf64a-242">Falso</span><span class="sxs-lookup"><span data-stu-id="bf64a-242">False</span></span>                                                                                                      |
| <span data-ttu-id="bf64a-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bf64a-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf64a-244">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bf64a-244">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="bf64a-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf64a-245">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="bf64a-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf64a-246">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="bf64a-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf64a-247">Search-Flags</span></span>           | <span data-ttu-id="bf64a-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf64a-248">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="bf64a-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf64a-249">System-Flags</span></span>           | <span data-ttu-id="bf64a-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf64a-250">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="bf64a-251">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bf64a-251">Classes used in</span></span>        | [<span data-ttu-id="bf64a-252">**Transporte entre sites**</span><span class="sxs-lookup"><span data-stu-id="bf64a-252">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="bf64a-253">**Link de site**</span><span class="sxs-lookup"><span data-stu-id="bf64a-253">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bf64a-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bf64a-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bf64a-255">Entrada</span><span class="sxs-lookup"><span data-stu-id="bf64a-255">Entry</span></span> | <span data-ttu-id="bf64a-256">Valor</span><span class="sxs-lookup"><span data-stu-id="bf64a-256">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf64a-257">ID do link</span><span class="sxs-lookup"><span data-stu-id="bf64a-257">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="bf64a-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf64a-258">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="bf64a-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf64a-259">System-Only</span></span>            | <span data-ttu-id="bf64a-260">Falso</span><span class="sxs-lookup"><span data-stu-id="bf64a-260">False</span></span>                                                                                                      |
| <span data-ttu-id="bf64a-261">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bf64a-261">Is-Single-Valued</span></span>       | <span data-ttu-id="bf64a-262">True</span><span class="sxs-lookup"><span data-stu-id="bf64a-262">True</span></span>                                                                                                       |
| <span data-ttu-id="bf64a-263">É indexado</span><span class="sxs-lookup"><span data-stu-id="bf64a-263">Is Indexed</span></span>             | <span data-ttu-id="bf64a-264">Falso</span><span class="sxs-lookup"><span data-stu-id="bf64a-264">False</span></span>                                                                                                      |
| <span data-ttu-id="bf64a-265">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bf64a-265">In Global Catalog</span></span>      | <span data-ttu-id="bf64a-266">Falso</span><span class="sxs-lookup"><span data-stu-id="bf64a-266">False</span></span>                                                                                                      |
| <span data-ttu-id="bf64a-267">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bf64a-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf64a-268">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bf64a-268">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="bf64a-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf64a-269">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="bf64a-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf64a-270">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="bf64a-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf64a-271">Search-Flags</span></span>           | <span data-ttu-id="bf64a-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf64a-272">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="bf64a-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf64a-273">System-Flags</span></span>           | <span data-ttu-id="bf64a-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf64a-274">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="bf64a-275">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bf64a-275">Classes used in</span></span>        | [<span data-ttu-id="bf64a-276">**Transporte entre sites**</span><span class="sxs-lookup"><span data-stu-id="bf64a-276">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="bf64a-277">**Link de site**</span><span class="sxs-lookup"><span data-stu-id="bf64a-277">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bf64a-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bf64a-278">Windows Server 2012</span></span>



| <span data-ttu-id="bf64a-279">Entrada</span><span class="sxs-lookup"><span data-stu-id="bf64a-279">Entry</span></span> | <span data-ttu-id="bf64a-280">Valor</span><span class="sxs-lookup"><span data-stu-id="bf64a-280">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf64a-281">ID do link</span><span class="sxs-lookup"><span data-stu-id="bf64a-281">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="bf64a-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf64a-282">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="bf64a-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf64a-283">System-Only</span></span>            | <span data-ttu-id="bf64a-284">Falso</span><span class="sxs-lookup"><span data-stu-id="bf64a-284">False</span></span>                                                                                                      |
| <span data-ttu-id="bf64a-285">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bf64a-285">Is-Single-Valued</span></span>       | <span data-ttu-id="bf64a-286">True</span><span class="sxs-lookup"><span data-stu-id="bf64a-286">True</span></span>                                                                                                       |
| <span data-ttu-id="bf64a-287">É indexado</span><span class="sxs-lookup"><span data-stu-id="bf64a-287">Is Indexed</span></span>             | <span data-ttu-id="bf64a-288">Falso</span><span class="sxs-lookup"><span data-stu-id="bf64a-288">False</span></span>                                                                                                      |
| <span data-ttu-id="bf64a-289">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bf64a-289">In Global Catalog</span></span>      | <span data-ttu-id="bf64a-290">Falso</span><span class="sxs-lookup"><span data-stu-id="bf64a-290">False</span></span>                                                                                                      |
| <span data-ttu-id="bf64a-291">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bf64a-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf64a-292">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bf64a-292">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="bf64a-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf64a-293">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="bf64a-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf64a-294">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="bf64a-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf64a-295">Search-Flags</span></span>           | <span data-ttu-id="bf64a-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf64a-296">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="bf64a-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf64a-297">System-Flags</span></span>           | <span data-ttu-id="bf64a-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf64a-298">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="bf64a-299">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bf64a-299">Classes used in</span></span>        | [<span data-ttu-id="bf64a-300">**Transporte entre sites**</span><span class="sxs-lookup"><span data-stu-id="bf64a-300">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="bf64a-301">**Link de site**</span><span class="sxs-lookup"><span data-stu-id="bf64a-301">**Site-Link**</span></span>](c-sitelink.md)<br/> |



 

 





