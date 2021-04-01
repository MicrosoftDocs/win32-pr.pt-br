---
title: atributo ms-DS-Replication-Notify-First-DSA-Delay
description: Esse atributo controla o atraso em tempo entre as alterações no DS e a notificação do primeiro parceiro de réplica para um NC.
ms.assetid: 58474bf9-9069-402a-a94b-4d1b6df0810e
ms.tgt_platform: multiple
keywords:
- ms-DS-Replication-Notificate-First-DSA-Delay esquema de atributo do AD
- atributo msDS-Replication-Notificate-First-DSA-Delay esquema do AD
topic_type:
- apiref
api_name:
- ms-DS-Replication-Notify-First-DSA-Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a981ff257562e701b12e3855b279b7995721e39
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825188"
---
# <a name="ms-ds-replication-notify-first-dsa-delay-attribute"></a><span data-ttu-id="cec18-105">atributo ms-DS-Replication-Notify-First-DSA-Delay</span><span class="sxs-lookup"><span data-stu-id="cec18-105">ms-DS-Replication-Notify-First-DSA-Delay attribute</span></span>

<span data-ttu-id="cec18-106">Esse atributo controla o atraso em tempo entre as alterações no DS e a notificação do primeiro parceiro de réplica para um NC.</span><span class="sxs-lookup"><span data-stu-id="cec18-106">This attribute controls the delay in time between changes to the DS, and notification of the first replica partner for an NC.</span></span>



| <span data-ttu-id="cec18-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="cec18-107">Entry</span></span> | <span data-ttu-id="cec18-108">Valor</span><span class="sxs-lookup"><span data-stu-id="cec18-108">Value</span></span> |
|-------------------|------------------------------------------|
| <span data-ttu-id="cec18-109">CN</span><span class="sxs-lookup"><span data-stu-id="cec18-109">CN</span></span>                | <span data-ttu-id="cec18-110">ms-DS-Replication-Notify-First-DSA-Delay</span><span class="sxs-lookup"><span data-stu-id="cec18-110">ms-DS-Replication-Notify-First-DSA-Delay</span></span> |
| <span data-ttu-id="cec18-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="cec18-111">Ldap-Display-Name</span></span> | <span data-ttu-id="cec18-112">msDS-Replication-Notify-primeiro-DSA-Delay</span><span class="sxs-lookup"><span data-stu-id="cec18-112">msDS-Replication-Notify-First-DSA-Delay</span></span>  |
| <span data-ttu-id="cec18-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="cec18-113">Size</span></span>              | \-                                       |
| <span data-ttu-id="cec18-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="cec18-114">Update Privilege</span></span>  | <span data-ttu-id="cec18-115">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="cec18-115">This value is set by the system.</span></span>         |
| <span data-ttu-id="cec18-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="cec18-116">Update Frequency</span></span>  | \-                                       |
| <span data-ttu-id="cec18-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cec18-117">Attribute-Id</span></span>      | <span data-ttu-id="cec18-118">1.2.840.113556.1.4.1663</span><span class="sxs-lookup"><span data-stu-id="cec18-118">1.2.840.113556.1.4.1663</span></span>                  |
| <span data-ttu-id="cec18-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="cec18-119">System-Id-Guid</span></span>    | <span data-ttu-id="cec18-120">85abd4f4-0a89-4e49-bdec-6f35bb2562ba</span><span class="sxs-lookup"><span data-stu-id="cec18-120">85abd4f4-0a89-4e49-bdec-6f35bb2562ba</span></span>     |
| <span data-ttu-id="cec18-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="cec18-121">Syntax</span></span>            | [<span data-ttu-id="cec18-122">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="cec18-122">**Enumeration**</span></span>](s-enumeration.md)     |



## <a name="implementations"></a><span data-ttu-id="cec18-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="cec18-123">Implementations</span></span>

-   [<span data-ttu-id="cec18-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cec18-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cec18-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="cec18-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="cec18-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cec18-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cec18-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cec18-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cec18-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cec18-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cec18-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cec18-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="cec18-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cec18-130">Windows Server 2003</span></span>



| <span data-ttu-id="cec18-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="cec18-131">Entry</span></span> | <span data-ttu-id="cec18-132">Valor</span><span class="sxs-lookup"><span data-stu-id="cec18-132">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="cec18-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="cec18-133">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="cec18-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cec18-134">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="cec18-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="cec18-135">System-Only</span></span>            | <span data-ttu-id="cec18-136">Falso</span><span class="sxs-lookup"><span data-stu-id="cec18-136">False</span></span>                                      |
| <span data-ttu-id="cec18-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cec18-137">Is-Single-Valued</span></span>       | <span data-ttu-id="cec18-138">True</span><span class="sxs-lookup"><span data-stu-id="cec18-138">True</span></span>                                       |
| <span data-ttu-id="cec18-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="cec18-139">Is Indexed</span></span>             | <span data-ttu-id="cec18-140">Falso</span><span class="sxs-lookup"><span data-stu-id="cec18-140">False</span></span>                                      |
| <span data-ttu-id="cec18-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cec18-141">In Global Catalog</span></span>      | <span data-ttu-id="cec18-142">Falso</span><span class="sxs-lookup"><span data-stu-id="cec18-142">False</span></span>                                      |
| <span data-ttu-id="cec18-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cec18-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="cec18-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cec18-144">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="cec18-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cec18-145">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="cec18-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cec18-146">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="cec18-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cec18-147">Search-Flags</span></span>           | <span data-ttu-id="cec18-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cec18-148">0x00000000</span></span>                                 |
| <span data-ttu-id="cec18-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cec18-149">System-Flags</span></span>           | <span data-ttu-id="cec18-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cec18-150">0x00000010</span></span>                                 |
| <span data-ttu-id="cec18-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cec18-151">Classes used in</span></span>        | [<span data-ttu-id="cec18-152">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="cec18-152">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="cec18-153">ADAM</span><span class="sxs-lookup"><span data-stu-id="cec18-153">ADAM</span></span>



| <span data-ttu-id="cec18-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="cec18-154">Entry</span></span> | <span data-ttu-id="cec18-155">Valor</span><span class="sxs-lookup"><span data-stu-id="cec18-155">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="cec18-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="cec18-156">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="cec18-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cec18-157">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="cec18-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="cec18-158">System-Only</span></span>            | <span data-ttu-id="cec18-159">Falso</span><span class="sxs-lookup"><span data-stu-id="cec18-159">False</span></span>                                      |
| <span data-ttu-id="cec18-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cec18-160">Is-Single-Valued</span></span>       | <span data-ttu-id="cec18-161">True</span><span class="sxs-lookup"><span data-stu-id="cec18-161">True</span></span>                                       |
| <span data-ttu-id="cec18-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="cec18-162">Is Indexed</span></span>             | <span data-ttu-id="cec18-163">Falso</span><span class="sxs-lookup"><span data-stu-id="cec18-163">False</span></span>                                      |
| <span data-ttu-id="cec18-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cec18-164">In Global Catalog</span></span>      | <span data-ttu-id="cec18-165">Falso</span><span class="sxs-lookup"><span data-stu-id="cec18-165">False</span></span>                                      |
| <span data-ttu-id="cec18-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cec18-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="cec18-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cec18-167">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="cec18-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cec18-168">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="cec18-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cec18-169">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="cec18-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cec18-170">Search-Flags</span></span>           | <span data-ttu-id="cec18-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cec18-171">0x00000000</span></span>                                 |
| <span data-ttu-id="cec18-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cec18-172">System-Flags</span></span>           | <span data-ttu-id="cec18-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cec18-173">0x00000010</span></span>                                 |
| <span data-ttu-id="cec18-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cec18-174">Classes used in</span></span>        | [<span data-ttu-id="cec18-175">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="cec18-175">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cec18-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cec18-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cec18-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="cec18-177">Entry</span></span> | <span data-ttu-id="cec18-178">Valor</span><span class="sxs-lookup"><span data-stu-id="cec18-178">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="cec18-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="cec18-179">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="cec18-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cec18-180">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="cec18-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="cec18-181">System-Only</span></span>            | <span data-ttu-id="cec18-182">Falso</span><span class="sxs-lookup"><span data-stu-id="cec18-182">False</span></span>                                      |
| <span data-ttu-id="cec18-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cec18-183">Is-Single-Valued</span></span>       | <span data-ttu-id="cec18-184">True</span><span class="sxs-lookup"><span data-stu-id="cec18-184">True</span></span>                                       |
| <span data-ttu-id="cec18-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="cec18-185">Is Indexed</span></span>             | <span data-ttu-id="cec18-186">Falso</span><span class="sxs-lookup"><span data-stu-id="cec18-186">False</span></span>                                      |
| <span data-ttu-id="cec18-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cec18-187">In Global Catalog</span></span>      | <span data-ttu-id="cec18-188">Falso</span><span class="sxs-lookup"><span data-stu-id="cec18-188">False</span></span>                                      |
| <span data-ttu-id="cec18-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cec18-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="cec18-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cec18-190">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="cec18-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cec18-191">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="cec18-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cec18-192">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="cec18-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cec18-193">Search-Flags</span></span>           | <span data-ttu-id="cec18-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cec18-194">0x00000000</span></span>                                 |
| <span data-ttu-id="cec18-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cec18-195">System-Flags</span></span>           | <span data-ttu-id="cec18-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cec18-196">0x00000010</span></span>                                 |
| <span data-ttu-id="cec18-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cec18-197">Classes used in</span></span>        | [<span data-ttu-id="cec18-198">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="cec18-198">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cec18-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cec18-199">Windows Server 2008</span></span>



| <span data-ttu-id="cec18-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="cec18-200">Entry</span></span> | <span data-ttu-id="cec18-201">Valor</span><span class="sxs-lookup"><span data-stu-id="cec18-201">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="cec18-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="cec18-202">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="cec18-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cec18-203">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="cec18-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="cec18-204">System-Only</span></span>            | <span data-ttu-id="cec18-205">Falso</span><span class="sxs-lookup"><span data-stu-id="cec18-205">False</span></span>                                      |
| <span data-ttu-id="cec18-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cec18-206">Is-Single-Valued</span></span>       | <span data-ttu-id="cec18-207">True</span><span class="sxs-lookup"><span data-stu-id="cec18-207">True</span></span>                                       |
| <span data-ttu-id="cec18-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="cec18-208">Is Indexed</span></span>             | <span data-ttu-id="cec18-209">Falso</span><span class="sxs-lookup"><span data-stu-id="cec18-209">False</span></span>                                      |
| <span data-ttu-id="cec18-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cec18-210">In Global Catalog</span></span>      | <span data-ttu-id="cec18-211">Falso</span><span class="sxs-lookup"><span data-stu-id="cec18-211">False</span></span>                                      |
| <span data-ttu-id="cec18-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cec18-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="cec18-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cec18-213">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="cec18-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cec18-214">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="cec18-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cec18-215">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="cec18-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cec18-216">Search-Flags</span></span>           | <span data-ttu-id="cec18-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cec18-217">0x00000000</span></span>                                 |
| <span data-ttu-id="cec18-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cec18-218">System-Flags</span></span>           | <span data-ttu-id="cec18-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cec18-219">0x00000010</span></span>                                 |
| <span data-ttu-id="cec18-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cec18-220">Classes used in</span></span>        | [<span data-ttu-id="cec18-221">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="cec18-221">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cec18-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cec18-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cec18-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="cec18-223">Entry</span></span> | <span data-ttu-id="cec18-224">Valor</span><span class="sxs-lookup"><span data-stu-id="cec18-224">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="cec18-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="cec18-225">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="cec18-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cec18-226">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="cec18-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="cec18-227">System-Only</span></span>            | <span data-ttu-id="cec18-228">Falso</span><span class="sxs-lookup"><span data-stu-id="cec18-228">False</span></span>                                      |
| <span data-ttu-id="cec18-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cec18-229">Is-Single-Valued</span></span>       | <span data-ttu-id="cec18-230">True</span><span class="sxs-lookup"><span data-stu-id="cec18-230">True</span></span>                                       |
| <span data-ttu-id="cec18-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="cec18-231">Is Indexed</span></span>             | <span data-ttu-id="cec18-232">Falso</span><span class="sxs-lookup"><span data-stu-id="cec18-232">False</span></span>                                      |
| <span data-ttu-id="cec18-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cec18-233">In Global Catalog</span></span>      | <span data-ttu-id="cec18-234">Falso</span><span class="sxs-lookup"><span data-stu-id="cec18-234">False</span></span>                                      |
| <span data-ttu-id="cec18-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cec18-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="cec18-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cec18-236">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="cec18-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cec18-237">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="cec18-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cec18-238">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="cec18-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cec18-239">Search-Flags</span></span>           | <span data-ttu-id="cec18-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cec18-240">0x00000000</span></span>                                 |
| <span data-ttu-id="cec18-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cec18-241">System-Flags</span></span>           | <span data-ttu-id="cec18-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cec18-242">0x00000010</span></span>                                 |
| <span data-ttu-id="cec18-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cec18-243">Classes used in</span></span>        | [<span data-ttu-id="cec18-244">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="cec18-244">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cec18-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cec18-245">Windows Server 2012</span></span>



| <span data-ttu-id="cec18-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="cec18-246">Entry</span></span> | <span data-ttu-id="cec18-247">Valor</span><span class="sxs-lookup"><span data-stu-id="cec18-247">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="cec18-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="cec18-248">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="cec18-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cec18-249">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="cec18-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="cec18-250">System-Only</span></span>            | <span data-ttu-id="cec18-251">Falso</span><span class="sxs-lookup"><span data-stu-id="cec18-251">False</span></span>                                      |
| <span data-ttu-id="cec18-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cec18-252">Is-Single-Valued</span></span>       | <span data-ttu-id="cec18-253">True</span><span class="sxs-lookup"><span data-stu-id="cec18-253">True</span></span>                                       |
| <span data-ttu-id="cec18-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="cec18-254">Is Indexed</span></span>             | <span data-ttu-id="cec18-255">Falso</span><span class="sxs-lookup"><span data-stu-id="cec18-255">False</span></span>                                      |
| <span data-ttu-id="cec18-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cec18-256">In Global Catalog</span></span>      | <span data-ttu-id="cec18-257">Falso</span><span class="sxs-lookup"><span data-stu-id="cec18-257">False</span></span>                                      |
| <span data-ttu-id="cec18-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cec18-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="cec18-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cec18-259">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="cec18-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cec18-260">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="cec18-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cec18-261">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="cec18-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cec18-262">Search-Flags</span></span>           | <span data-ttu-id="cec18-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cec18-263">0x00000000</span></span>                                 |
| <span data-ttu-id="cec18-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cec18-264">System-Flags</span></span>           | <span data-ttu-id="cec18-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cec18-265">0x00000010</span></span>                                 |
| <span data-ttu-id="cec18-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cec18-266">Classes used in</span></span>        | [<span data-ttu-id="cec18-267">**Referência cruzada**</span><span class="sxs-lookup"><span data-stu-id="cec18-267">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





