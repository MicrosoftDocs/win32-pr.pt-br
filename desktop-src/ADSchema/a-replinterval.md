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
# <a name="repl-interval-attribute"></a><span data-ttu-id="2302d-105">Repl-Interval atributo</span><span class="sxs-lookup"><span data-stu-id="2302d-105">Repl-Interval attribute</span></span>

<span data-ttu-id="2302d-106">O atributo de objetos Site-Link que define o intervalo, em minutos, entre os ciclos de replicação entre os sites na lista de sites.</span><span class="sxs-lookup"><span data-stu-id="2302d-106">The attribute of Site-Link objects that defines the interval, in minutes, between replication cycles between the sites in the Site-List.</span></span> <span data-ttu-id="2302d-107">Deve ser um múltiplo de 15 minutos (a granularidade da replicação de DS entre sites), um mínimo de 15 minutos e um máximo de 10.080 minutos (uma semana).</span><span class="sxs-lookup"><span data-stu-id="2302d-107">Must be a multiple of 15 minutes (the granularity of cross-site DS replication), a minimum of 15 minutes, and a maximum of 10,080 minutes (one week).</span></span>



| <span data-ttu-id="2302d-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="2302d-108">Entry</span></span> | <span data-ttu-id="2302d-109">Valor</span><span class="sxs-lookup"><span data-stu-id="2302d-109">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="2302d-110">CN</span><span class="sxs-lookup"><span data-stu-id="2302d-110">CN</span></span>                | <span data-ttu-id="2302d-111">Repl-Interval</span><span class="sxs-lookup"><span data-stu-id="2302d-111">Repl-Interval</span></span>                                  |
| <span data-ttu-id="2302d-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2302d-112">Ldap-Display-Name</span></span> | <span data-ttu-id="2302d-113">replInterval</span><span class="sxs-lookup"><span data-stu-id="2302d-113">replInterval</span></span>                                   |
| <span data-ttu-id="2302d-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="2302d-114">Size</span></span>              | <span data-ttu-id="2302d-115">4 bytes</span><span class="sxs-lookup"><span data-stu-id="2302d-115">4 bytes</span></span>                                        |
| <span data-ttu-id="2302d-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="2302d-116">Update Privilege</span></span>  | <span data-ttu-id="2302d-117">Administrador corporativo</span><span class="sxs-lookup"><span data-stu-id="2302d-117">Enterprise administrator</span></span>                       |
| <span data-ttu-id="2302d-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="2302d-118">Update Frequency</span></span>  | <span data-ttu-id="2302d-119">Quando o intervalo de replicação precisa ser alterado.</span><span class="sxs-lookup"><span data-stu-id="2302d-119">When the replication interval needs to change.</span></span> |
| <span data-ttu-id="2302d-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2302d-120">Attribute-Id</span></span>      | <span data-ttu-id="2302d-121">1.2.840.113556.1.4.1336</span><span class="sxs-lookup"><span data-stu-id="2302d-121">1.2.840.113556.1.4.1336</span></span>                        |
| <span data-ttu-id="2302d-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2302d-122">System-Id-Guid</span></span>    | <span data-ttu-id="2302d-123">45ba9d1a-56fa-11d2-90d0-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="2302d-123">45ba9d1a-56fa-11d2-90d0-00c04fd91ab1</span></span>           |
| <span data-ttu-id="2302d-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="2302d-124">Syntax</span></span>            | [<span data-ttu-id="2302d-125">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="2302d-125">**Enumeration**</span></span>](s-enumeration.md)           |



## <a name="implementations"></a><span data-ttu-id="2302d-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="2302d-126">Implementations</span></span>

-   [<span data-ttu-id="2302d-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2302d-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2302d-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2302d-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2302d-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="2302d-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="2302d-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2302d-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2302d-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2302d-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2302d-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2302d-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2302d-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2302d-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2302d-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2302d-134">Windows 2000 Server</span></span>



| <span data-ttu-id="2302d-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="2302d-135">Entry</span></span> | <span data-ttu-id="2302d-136">Valor</span><span class="sxs-lookup"><span data-stu-id="2302d-136">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2302d-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="2302d-137">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="2302d-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2302d-138">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="2302d-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="2302d-139">System-Only</span></span>            | <span data-ttu-id="2302d-140">Falso</span><span class="sxs-lookup"><span data-stu-id="2302d-140">False</span></span>                                                                                                      |
| <span data-ttu-id="2302d-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2302d-141">Is-Single-Valued</span></span>       | <span data-ttu-id="2302d-142">True</span><span class="sxs-lookup"><span data-stu-id="2302d-142">True</span></span>                                                                                                       |
| <span data-ttu-id="2302d-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="2302d-143">Is Indexed</span></span>             | <span data-ttu-id="2302d-144">Falso</span><span class="sxs-lookup"><span data-stu-id="2302d-144">False</span></span>                                                                                                      |
| <span data-ttu-id="2302d-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2302d-145">In Global Catalog</span></span>      | <span data-ttu-id="2302d-146">Falso</span><span class="sxs-lookup"><span data-stu-id="2302d-146">False</span></span>                                                                                                      |
| <span data-ttu-id="2302d-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2302d-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="2302d-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2302d-148">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="2302d-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2302d-149">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="2302d-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2302d-150">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="2302d-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2302d-151">Search-Flags</span></span>           | <span data-ttu-id="2302d-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2302d-152">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="2302d-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2302d-153">System-Flags</span></span>           | <span data-ttu-id="2302d-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2302d-154">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="2302d-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2302d-155">Classes used in</span></span>        | [<span data-ttu-id="2302d-156">**Transporte entre sites**</span><span class="sxs-lookup"><span data-stu-id="2302d-156">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="2302d-157">**Link de site**</span><span class="sxs-lookup"><span data-stu-id="2302d-157">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2302d-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2302d-158">Windows Server 2003</span></span>



| <span data-ttu-id="2302d-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="2302d-159">Entry</span></span> | <span data-ttu-id="2302d-160">Valor</span><span class="sxs-lookup"><span data-stu-id="2302d-160">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2302d-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="2302d-161">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="2302d-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2302d-162">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="2302d-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="2302d-163">System-Only</span></span>            | <span data-ttu-id="2302d-164">Falso</span><span class="sxs-lookup"><span data-stu-id="2302d-164">False</span></span>                                                                                                      |
| <span data-ttu-id="2302d-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2302d-165">Is-Single-Valued</span></span>       | <span data-ttu-id="2302d-166">True</span><span class="sxs-lookup"><span data-stu-id="2302d-166">True</span></span>                                                                                                       |
| <span data-ttu-id="2302d-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="2302d-167">Is Indexed</span></span>             | <span data-ttu-id="2302d-168">Falso</span><span class="sxs-lookup"><span data-stu-id="2302d-168">False</span></span>                                                                                                      |
| <span data-ttu-id="2302d-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2302d-169">In Global Catalog</span></span>      | <span data-ttu-id="2302d-170">Falso</span><span class="sxs-lookup"><span data-stu-id="2302d-170">False</span></span>                                                                                                      |
| <span data-ttu-id="2302d-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2302d-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="2302d-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2302d-172">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="2302d-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2302d-173">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="2302d-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2302d-174">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="2302d-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2302d-175">Search-Flags</span></span>           | <span data-ttu-id="2302d-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2302d-176">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="2302d-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2302d-177">System-Flags</span></span>           | <span data-ttu-id="2302d-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2302d-178">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="2302d-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2302d-179">Classes used in</span></span>        | [<span data-ttu-id="2302d-180">**Transporte entre sites**</span><span class="sxs-lookup"><span data-stu-id="2302d-180">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="2302d-181">**Link de site**</span><span class="sxs-lookup"><span data-stu-id="2302d-181">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="adam"></a><span data-ttu-id="2302d-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="2302d-182">ADAM</span></span>



| <span data-ttu-id="2302d-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="2302d-183">Entry</span></span> | <span data-ttu-id="2302d-184">Valor</span><span class="sxs-lookup"><span data-stu-id="2302d-184">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2302d-185">ID do link</span><span class="sxs-lookup"><span data-stu-id="2302d-185">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="2302d-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2302d-186">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="2302d-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="2302d-187">System-Only</span></span>            | <span data-ttu-id="2302d-188">Falso</span><span class="sxs-lookup"><span data-stu-id="2302d-188">False</span></span>                                                                                                      |
| <span data-ttu-id="2302d-189">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2302d-189">Is-Single-Valued</span></span>       | <span data-ttu-id="2302d-190">True</span><span class="sxs-lookup"><span data-stu-id="2302d-190">True</span></span>                                                                                                       |
| <span data-ttu-id="2302d-191">É indexado</span><span class="sxs-lookup"><span data-stu-id="2302d-191">Is Indexed</span></span>             | <span data-ttu-id="2302d-192">Falso</span><span class="sxs-lookup"><span data-stu-id="2302d-192">False</span></span>                                                                                                      |
| <span data-ttu-id="2302d-193">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2302d-193">In Global Catalog</span></span>      | <span data-ttu-id="2302d-194">Falso</span><span class="sxs-lookup"><span data-stu-id="2302d-194">False</span></span>                                                                                                      |
| <span data-ttu-id="2302d-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2302d-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="2302d-196">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2302d-196">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="2302d-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2302d-197">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="2302d-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2302d-198">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="2302d-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2302d-199">Search-Flags</span></span>           | <span data-ttu-id="2302d-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2302d-200">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="2302d-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2302d-201">System-Flags</span></span>           | <span data-ttu-id="2302d-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2302d-202">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="2302d-203">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2302d-203">Classes used in</span></span>        | [<span data-ttu-id="2302d-204">**Transporte entre sites**</span><span class="sxs-lookup"><span data-stu-id="2302d-204">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="2302d-205">**Link de site**</span><span class="sxs-lookup"><span data-stu-id="2302d-205">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2302d-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2302d-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2302d-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="2302d-207">Entry</span></span> | <span data-ttu-id="2302d-208">Valor</span><span class="sxs-lookup"><span data-stu-id="2302d-208">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2302d-209">ID do link</span><span class="sxs-lookup"><span data-stu-id="2302d-209">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="2302d-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2302d-210">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="2302d-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="2302d-211">System-Only</span></span>            | <span data-ttu-id="2302d-212">Falso</span><span class="sxs-lookup"><span data-stu-id="2302d-212">False</span></span>                                                                                                      |
| <span data-ttu-id="2302d-213">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2302d-213">Is-Single-Valued</span></span>       | <span data-ttu-id="2302d-214">True</span><span class="sxs-lookup"><span data-stu-id="2302d-214">True</span></span>                                                                                                       |
| <span data-ttu-id="2302d-215">É indexado</span><span class="sxs-lookup"><span data-stu-id="2302d-215">Is Indexed</span></span>             | <span data-ttu-id="2302d-216">Falso</span><span class="sxs-lookup"><span data-stu-id="2302d-216">False</span></span>                                                                                                      |
| <span data-ttu-id="2302d-217">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2302d-217">In Global Catalog</span></span>      | <span data-ttu-id="2302d-218">Falso</span><span class="sxs-lookup"><span data-stu-id="2302d-218">False</span></span>                                                                                                      |
| <span data-ttu-id="2302d-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2302d-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="2302d-220">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2302d-220">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="2302d-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2302d-221">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="2302d-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2302d-222">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="2302d-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2302d-223">Search-Flags</span></span>           | <span data-ttu-id="2302d-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2302d-224">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="2302d-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2302d-225">System-Flags</span></span>           | <span data-ttu-id="2302d-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2302d-226">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="2302d-227">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2302d-227">Classes used in</span></span>        | [<span data-ttu-id="2302d-228">**Transporte entre sites**</span><span class="sxs-lookup"><span data-stu-id="2302d-228">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="2302d-229">**Link de site**</span><span class="sxs-lookup"><span data-stu-id="2302d-229">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2302d-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2302d-230">Windows Server 2008</span></span>



| <span data-ttu-id="2302d-231">Entrada</span><span class="sxs-lookup"><span data-stu-id="2302d-231">Entry</span></span> | <span data-ttu-id="2302d-232">Valor</span><span class="sxs-lookup"><span data-stu-id="2302d-232">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2302d-233">ID do link</span><span class="sxs-lookup"><span data-stu-id="2302d-233">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="2302d-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2302d-234">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="2302d-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="2302d-235">System-Only</span></span>            | <span data-ttu-id="2302d-236">Falso</span><span class="sxs-lookup"><span data-stu-id="2302d-236">False</span></span>                                                                                                      |
| <span data-ttu-id="2302d-237">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2302d-237">Is-Single-Valued</span></span>       | <span data-ttu-id="2302d-238">True</span><span class="sxs-lookup"><span data-stu-id="2302d-238">True</span></span>                                                                                                       |
| <span data-ttu-id="2302d-239">É indexado</span><span class="sxs-lookup"><span data-stu-id="2302d-239">Is Indexed</span></span>             | <span data-ttu-id="2302d-240">Falso</span><span class="sxs-lookup"><span data-stu-id="2302d-240">False</span></span>                                                                                                      |
| <span data-ttu-id="2302d-241">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2302d-241">In Global Catalog</span></span>      | <span data-ttu-id="2302d-242">Falso</span><span class="sxs-lookup"><span data-stu-id="2302d-242">False</span></span>                                                                                                      |
| <span data-ttu-id="2302d-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2302d-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="2302d-244">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2302d-244">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="2302d-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2302d-245">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="2302d-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2302d-246">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="2302d-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2302d-247">Search-Flags</span></span>           | <span data-ttu-id="2302d-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2302d-248">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="2302d-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2302d-249">System-Flags</span></span>           | <span data-ttu-id="2302d-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2302d-250">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="2302d-251">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2302d-251">Classes used in</span></span>        | [<span data-ttu-id="2302d-252">**Transporte entre sites**</span><span class="sxs-lookup"><span data-stu-id="2302d-252">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="2302d-253">**Link de site**</span><span class="sxs-lookup"><span data-stu-id="2302d-253">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2302d-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2302d-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2302d-255">Entrada</span><span class="sxs-lookup"><span data-stu-id="2302d-255">Entry</span></span> | <span data-ttu-id="2302d-256">Valor</span><span class="sxs-lookup"><span data-stu-id="2302d-256">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2302d-257">ID do link</span><span class="sxs-lookup"><span data-stu-id="2302d-257">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="2302d-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2302d-258">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="2302d-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="2302d-259">System-Only</span></span>            | <span data-ttu-id="2302d-260">Falso</span><span class="sxs-lookup"><span data-stu-id="2302d-260">False</span></span>                                                                                                      |
| <span data-ttu-id="2302d-261">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2302d-261">Is-Single-Valued</span></span>       | <span data-ttu-id="2302d-262">True</span><span class="sxs-lookup"><span data-stu-id="2302d-262">True</span></span>                                                                                                       |
| <span data-ttu-id="2302d-263">É indexado</span><span class="sxs-lookup"><span data-stu-id="2302d-263">Is Indexed</span></span>             | <span data-ttu-id="2302d-264">Falso</span><span class="sxs-lookup"><span data-stu-id="2302d-264">False</span></span>                                                                                                      |
| <span data-ttu-id="2302d-265">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2302d-265">In Global Catalog</span></span>      | <span data-ttu-id="2302d-266">Falso</span><span class="sxs-lookup"><span data-stu-id="2302d-266">False</span></span>                                                                                                      |
| <span data-ttu-id="2302d-267">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2302d-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="2302d-268">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2302d-268">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="2302d-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2302d-269">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="2302d-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2302d-270">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="2302d-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2302d-271">Search-Flags</span></span>           | <span data-ttu-id="2302d-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2302d-272">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="2302d-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2302d-273">System-Flags</span></span>           | <span data-ttu-id="2302d-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2302d-274">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="2302d-275">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2302d-275">Classes used in</span></span>        | [<span data-ttu-id="2302d-276">**Transporte entre sites**</span><span class="sxs-lookup"><span data-stu-id="2302d-276">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="2302d-277">**Link de site**</span><span class="sxs-lookup"><span data-stu-id="2302d-277">**Site-Link**</span></span>](c-sitelink.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2302d-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2302d-278">Windows Server 2012</span></span>



| <span data-ttu-id="2302d-279">Entrada</span><span class="sxs-lookup"><span data-stu-id="2302d-279">Entry</span></span> | <span data-ttu-id="2302d-280">Valor</span><span class="sxs-lookup"><span data-stu-id="2302d-280">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2302d-281">ID do link</span><span class="sxs-lookup"><span data-stu-id="2302d-281">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="2302d-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2302d-282">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="2302d-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="2302d-283">System-Only</span></span>            | <span data-ttu-id="2302d-284">Falso</span><span class="sxs-lookup"><span data-stu-id="2302d-284">False</span></span>                                                                                                      |
| <span data-ttu-id="2302d-285">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2302d-285">Is-Single-Valued</span></span>       | <span data-ttu-id="2302d-286">True</span><span class="sxs-lookup"><span data-stu-id="2302d-286">True</span></span>                                                                                                       |
| <span data-ttu-id="2302d-287">É indexado</span><span class="sxs-lookup"><span data-stu-id="2302d-287">Is Indexed</span></span>             | <span data-ttu-id="2302d-288">Falso</span><span class="sxs-lookup"><span data-stu-id="2302d-288">False</span></span>                                                                                                      |
| <span data-ttu-id="2302d-289">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2302d-289">In Global Catalog</span></span>      | <span data-ttu-id="2302d-290">Falso</span><span class="sxs-lookup"><span data-stu-id="2302d-290">False</span></span>                                                                                                      |
| <span data-ttu-id="2302d-291">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2302d-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="2302d-292">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2302d-292">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="2302d-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2302d-293">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="2302d-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2302d-294">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="2302d-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2302d-295">Search-Flags</span></span>           | <span data-ttu-id="2302d-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2302d-296">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="2302d-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2302d-297">System-Flags</span></span>           | <span data-ttu-id="2302d-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2302d-298">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="2302d-299">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2302d-299">Classes used in</span></span>        | [<span data-ttu-id="2302d-300">**Transporte entre sites**</span><span class="sxs-lookup"><span data-stu-id="2302d-300">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> [<span data-ttu-id="2302d-301">**Link de site**</span><span class="sxs-lookup"><span data-stu-id="2302d-301">**Site-Link**</span></span>](c-sitelink.md)<br/> |



 

 





