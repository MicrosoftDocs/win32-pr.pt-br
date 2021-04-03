---
title: Seq-Notification atributo
description: Esse atributo contém um contador que é incrementado diariamente. Esse valor de contador é fornecido ao serviço de rastreamento de link que adiciona o valor a seus volumes e os arquivos de origem do link quando eles são atualizados. O controlador de domínio mantém esse valor.
ms.assetid: 63fbded5-a21f-4a0e-aadc-568e199e8b9e
ms.tgt_platform: multiple
keywords:
- Esquema de Seq-Notification do atributo AD
- Esquema de AD do atributo seqNotification
topic_type:
- apiref
api_name:
- Seq-Notification
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31fc3abc61a8102ced02c87897d5e7a4f706dbbb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086841"
---
# <a name="seq-notification-attribute"></a><span data-ttu-id="cb8d1-107">Seq-Notification atributo</span><span class="sxs-lookup"><span data-stu-id="cb8d1-107">Seq-Notification attribute</span></span>

<span data-ttu-id="cb8d1-108">Esse atributo contém um contador que é incrementado diariamente.</span><span class="sxs-lookup"><span data-stu-id="cb8d1-108">This attribute contains a counter that is incremented daily.</span></span> <span data-ttu-id="cb8d1-109">Esse valor de contador é fornecido ao serviço de rastreamento de link que adiciona o valor a seus volumes e os arquivos de origem do link quando eles são atualizados.</span><span class="sxs-lookup"><span data-stu-id="cb8d1-109">This counter value is given to the link tracking service which adds the value to its volumes and link source files when they are refreshed.</span></span> <span data-ttu-id="cb8d1-110">O controlador de domínio mantém esse valor.</span><span class="sxs-lookup"><span data-stu-id="cb8d1-110">The domain controller maintains this value.</span></span>



| <span data-ttu-id="cb8d1-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="cb8d1-111">Entry</span></span> | <span data-ttu-id="cb8d1-112">Valor</span><span class="sxs-lookup"><span data-stu-id="cb8d1-112">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="cb8d1-113">CN</span><span class="sxs-lookup"><span data-stu-id="cb8d1-113">CN</span></span>                | <span data-ttu-id="cb8d1-114">Seq-Notification</span><span class="sxs-lookup"><span data-stu-id="cb8d1-114">Seq-Notification</span></span>                     |
| <span data-ttu-id="cb8d1-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="cb8d1-115">Ldap-Display-Name</span></span> | <span data-ttu-id="cb8d1-116">seqNotification</span><span class="sxs-lookup"><span data-stu-id="cb8d1-116">seqNotification</span></span>                      |
| <span data-ttu-id="cb8d1-117">Tamanho</span><span class="sxs-lookup"><span data-stu-id="cb8d1-117">Size</span></span>              | \-                                   |
| <span data-ttu-id="cb8d1-118">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="cb8d1-118">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="cb8d1-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="cb8d1-119">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="cb8d1-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cb8d1-120">Attribute-Id</span></span>      | <span data-ttu-id="cb8d1-121">1.2.840.113556.1.4.504</span><span class="sxs-lookup"><span data-stu-id="cb8d1-121">1.2.840.113556.1.4.504</span></span>               |
| <span data-ttu-id="cb8d1-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="cb8d1-122">System-Id-Guid</span></span>    | <span data-ttu-id="cb8d1-123">ddac0cf2-af8f-11d0-afeb-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="cb8d1-123">ddac0cf2-af8f-11d0-afeb-00c04fd930c9</span></span> |
| <span data-ttu-id="cb8d1-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb8d1-124">Syntax</span></span>            | [<span data-ttu-id="cb8d1-125">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="cb8d1-125">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="cb8d1-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="cb8d1-126">Implementations</span></span>

-   [<span data-ttu-id="cb8d1-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cb8d1-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cb8d1-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cb8d1-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cb8d1-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cb8d1-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cb8d1-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cb8d1-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cb8d1-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cb8d1-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cb8d1-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cb8d1-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cb8d1-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cb8d1-133">Windows 2000 Server</span></span>



| <span data-ttu-id="cb8d1-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="cb8d1-134">Entry</span></span> | <span data-ttu-id="cb8d1-135">Valor</span><span class="sxs-lookup"><span data-stu-id="cb8d1-135">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="cb8d1-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="cb8d1-136">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="cb8d1-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb8d1-137">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="cb8d1-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb8d1-138">System-Only</span></span>            | <span data-ttu-id="cb8d1-139">Falso</span><span class="sxs-lookup"><span data-stu-id="cb8d1-139">False</span></span>                                                          |
| <span data-ttu-id="cb8d1-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cb8d1-140">Is-Single-Valued</span></span>       | <span data-ttu-id="cb8d1-141">True</span><span class="sxs-lookup"><span data-stu-id="cb8d1-141">True</span></span>                                                           |
| <span data-ttu-id="cb8d1-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="cb8d1-142">Is Indexed</span></span>             | <span data-ttu-id="cb8d1-143">Falso</span><span class="sxs-lookup"><span data-stu-id="cb8d1-143">False</span></span>                                                          |
| <span data-ttu-id="cb8d1-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cb8d1-144">In Global Catalog</span></span>      | <span data-ttu-id="cb8d1-145">Falso</span><span class="sxs-lookup"><span data-stu-id="cb8d1-145">False</span></span>                                                          |
| <span data-ttu-id="cb8d1-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cb8d1-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb8d1-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cb8d1-147">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="cb8d1-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb8d1-148">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="cb8d1-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb8d1-149">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="cb8d1-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb8d1-150">Search-Flags</span></span>           | <span data-ttu-id="cb8d1-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb8d1-151">0x00000000</span></span>                                                     |
| <span data-ttu-id="cb8d1-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb8d1-152">System-Flags</span></span>           | <span data-ttu-id="cb8d1-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cb8d1-153">0x00000010</span></span>                                                     |
| <span data-ttu-id="cb8d1-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cb8d1-154">Classes used in</span></span>        | [<span data-ttu-id="cb8d1-155">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="cb8d1-155">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cb8d1-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cb8d1-156">Windows Server 2003</span></span>



| <span data-ttu-id="cb8d1-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="cb8d1-157">Entry</span></span> | <span data-ttu-id="cb8d1-158">Valor</span><span class="sxs-lookup"><span data-stu-id="cb8d1-158">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="cb8d1-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="cb8d1-159">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="cb8d1-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb8d1-160">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="cb8d1-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb8d1-161">System-Only</span></span>            | <span data-ttu-id="cb8d1-162">Falso</span><span class="sxs-lookup"><span data-stu-id="cb8d1-162">False</span></span>                                                          |
| <span data-ttu-id="cb8d1-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cb8d1-163">Is-Single-Valued</span></span>       | <span data-ttu-id="cb8d1-164">True</span><span class="sxs-lookup"><span data-stu-id="cb8d1-164">True</span></span>                                                           |
| <span data-ttu-id="cb8d1-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="cb8d1-165">Is Indexed</span></span>             | <span data-ttu-id="cb8d1-166">Falso</span><span class="sxs-lookup"><span data-stu-id="cb8d1-166">False</span></span>                                                          |
| <span data-ttu-id="cb8d1-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cb8d1-167">In Global Catalog</span></span>      | <span data-ttu-id="cb8d1-168">Falso</span><span class="sxs-lookup"><span data-stu-id="cb8d1-168">False</span></span>                                                          |
| <span data-ttu-id="cb8d1-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cb8d1-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb8d1-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cb8d1-170">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="cb8d1-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb8d1-171">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="cb8d1-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb8d1-172">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="cb8d1-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb8d1-173">Search-Flags</span></span>           | <span data-ttu-id="cb8d1-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb8d1-174">0x00000000</span></span>                                                     |
| <span data-ttu-id="cb8d1-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb8d1-175">System-Flags</span></span>           | <span data-ttu-id="cb8d1-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cb8d1-176">0x00000010</span></span>                                                     |
| <span data-ttu-id="cb8d1-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cb8d1-177">Classes used in</span></span>        | [<span data-ttu-id="cb8d1-178">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="cb8d1-178">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cb8d1-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cb8d1-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cb8d1-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="cb8d1-180">Entry</span></span> | <span data-ttu-id="cb8d1-181">Valor</span><span class="sxs-lookup"><span data-stu-id="cb8d1-181">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="cb8d1-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="cb8d1-182">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="cb8d1-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb8d1-183">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="cb8d1-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb8d1-184">System-Only</span></span>            | <span data-ttu-id="cb8d1-185">Falso</span><span class="sxs-lookup"><span data-stu-id="cb8d1-185">False</span></span>                                                          |
| <span data-ttu-id="cb8d1-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cb8d1-186">Is-Single-Valued</span></span>       | <span data-ttu-id="cb8d1-187">True</span><span class="sxs-lookup"><span data-stu-id="cb8d1-187">True</span></span>                                                           |
| <span data-ttu-id="cb8d1-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="cb8d1-188">Is Indexed</span></span>             | <span data-ttu-id="cb8d1-189">Falso</span><span class="sxs-lookup"><span data-stu-id="cb8d1-189">False</span></span>                                                          |
| <span data-ttu-id="cb8d1-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cb8d1-190">In Global Catalog</span></span>      | <span data-ttu-id="cb8d1-191">Falso</span><span class="sxs-lookup"><span data-stu-id="cb8d1-191">False</span></span>                                                          |
| <span data-ttu-id="cb8d1-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cb8d1-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb8d1-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cb8d1-193">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="cb8d1-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb8d1-194">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="cb8d1-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb8d1-195">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="cb8d1-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb8d1-196">Search-Flags</span></span>           | <span data-ttu-id="cb8d1-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb8d1-197">0x00000000</span></span>                                                     |
| <span data-ttu-id="cb8d1-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb8d1-198">System-Flags</span></span>           | <span data-ttu-id="cb8d1-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cb8d1-199">0x00000010</span></span>                                                     |
| <span data-ttu-id="cb8d1-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cb8d1-200">Classes used in</span></span>        | [<span data-ttu-id="cb8d1-201">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="cb8d1-201">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cb8d1-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cb8d1-202">Windows Server 2008</span></span>



| <span data-ttu-id="cb8d1-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="cb8d1-203">Entry</span></span> | <span data-ttu-id="cb8d1-204">Valor</span><span class="sxs-lookup"><span data-stu-id="cb8d1-204">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="cb8d1-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="cb8d1-205">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="cb8d1-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb8d1-206">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="cb8d1-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb8d1-207">System-Only</span></span>            | <span data-ttu-id="cb8d1-208">Falso</span><span class="sxs-lookup"><span data-stu-id="cb8d1-208">False</span></span>                                                          |
| <span data-ttu-id="cb8d1-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cb8d1-209">Is-Single-Valued</span></span>       | <span data-ttu-id="cb8d1-210">True</span><span class="sxs-lookup"><span data-stu-id="cb8d1-210">True</span></span>                                                           |
| <span data-ttu-id="cb8d1-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="cb8d1-211">Is Indexed</span></span>             | <span data-ttu-id="cb8d1-212">Falso</span><span class="sxs-lookup"><span data-stu-id="cb8d1-212">False</span></span>                                                          |
| <span data-ttu-id="cb8d1-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cb8d1-213">In Global Catalog</span></span>      | <span data-ttu-id="cb8d1-214">Falso</span><span class="sxs-lookup"><span data-stu-id="cb8d1-214">False</span></span>                                                          |
| <span data-ttu-id="cb8d1-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cb8d1-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb8d1-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cb8d1-216">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="cb8d1-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb8d1-217">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="cb8d1-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb8d1-218">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="cb8d1-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb8d1-219">Search-Flags</span></span>           | <span data-ttu-id="cb8d1-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb8d1-220">0x00000000</span></span>                                                     |
| <span data-ttu-id="cb8d1-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb8d1-221">System-Flags</span></span>           | <span data-ttu-id="cb8d1-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cb8d1-222">0x00000010</span></span>                                                     |
| <span data-ttu-id="cb8d1-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cb8d1-223">Classes used in</span></span>        | [<span data-ttu-id="cb8d1-224">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="cb8d1-224">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cb8d1-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cb8d1-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cb8d1-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="cb8d1-226">Entry</span></span> | <span data-ttu-id="cb8d1-227">Valor</span><span class="sxs-lookup"><span data-stu-id="cb8d1-227">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="cb8d1-228">ID do link</span><span class="sxs-lookup"><span data-stu-id="cb8d1-228">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="cb8d1-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb8d1-229">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="cb8d1-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb8d1-230">System-Only</span></span>            | <span data-ttu-id="cb8d1-231">Falso</span><span class="sxs-lookup"><span data-stu-id="cb8d1-231">False</span></span>                                                          |
| <span data-ttu-id="cb8d1-232">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cb8d1-232">Is-Single-Valued</span></span>       | <span data-ttu-id="cb8d1-233">True</span><span class="sxs-lookup"><span data-stu-id="cb8d1-233">True</span></span>                                                           |
| <span data-ttu-id="cb8d1-234">É indexado</span><span class="sxs-lookup"><span data-stu-id="cb8d1-234">Is Indexed</span></span>             | <span data-ttu-id="cb8d1-235">Falso</span><span class="sxs-lookup"><span data-stu-id="cb8d1-235">False</span></span>                                                          |
| <span data-ttu-id="cb8d1-236">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cb8d1-236">In Global Catalog</span></span>      | <span data-ttu-id="cb8d1-237">Falso</span><span class="sxs-lookup"><span data-stu-id="cb8d1-237">False</span></span>                                                          |
| <span data-ttu-id="cb8d1-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cb8d1-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb8d1-239">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cb8d1-239">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="cb8d1-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb8d1-240">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="cb8d1-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb8d1-241">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="cb8d1-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb8d1-242">Search-Flags</span></span>           | <span data-ttu-id="cb8d1-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb8d1-243">0x00000000</span></span>                                                     |
| <span data-ttu-id="cb8d1-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb8d1-244">System-Flags</span></span>           | <span data-ttu-id="cb8d1-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cb8d1-245">0x00000010</span></span>                                                     |
| <span data-ttu-id="cb8d1-246">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cb8d1-246">Classes used in</span></span>        | [<span data-ttu-id="cb8d1-247">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="cb8d1-247">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cb8d1-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cb8d1-248">Windows Server 2012</span></span>



| <span data-ttu-id="cb8d1-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="cb8d1-249">Entry</span></span> | <span data-ttu-id="cb8d1-250">Valor</span><span class="sxs-lookup"><span data-stu-id="cb8d1-250">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="cb8d1-251">ID do link</span><span class="sxs-lookup"><span data-stu-id="cb8d1-251">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="cb8d1-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cb8d1-252">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="cb8d1-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="cb8d1-253">System-Only</span></span>            | <span data-ttu-id="cb8d1-254">Falso</span><span class="sxs-lookup"><span data-stu-id="cb8d1-254">False</span></span>                                                          |
| <span data-ttu-id="cb8d1-255">É de valor único</span><span class="sxs-lookup"><span data-stu-id="cb8d1-255">Is-Single-Valued</span></span>       | <span data-ttu-id="cb8d1-256">True</span><span class="sxs-lookup"><span data-stu-id="cb8d1-256">True</span></span>                                                           |
| <span data-ttu-id="cb8d1-257">É indexado</span><span class="sxs-lookup"><span data-stu-id="cb8d1-257">Is Indexed</span></span>             | <span data-ttu-id="cb8d1-258">Falso</span><span class="sxs-lookup"><span data-stu-id="cb8d1-258">False</span></span>                                                          |
| <span data-ttu-id="cb8d1-259">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="cb8d1-259">In Global Catalog</span></span>      | <span data-ttu-id="cb8d1-260">Falso</span><span class="sxs-lookup"><span data-stu-id="cb8d1-260">False</span></span>                                                          |
| <span data-ttu-id="cb8d1-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="cb8d1-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="cb8d1-262">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="cb8d1-262">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="cb8d1-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cb8d1-263">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="cb8d1-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cb8d1-264">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="cb8d1-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cb8d1-265">Search-Flags</span></span>           | <span data-ttu-id="cb8d1-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb8d1-266">0x00000000</span></span>                                                     |
| <span data-ttu-id="cb8d1-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cb8d1-267">System-Flags</span></span>           | <span data-ttu-id="cb8d1-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cb8d1-268">0x00000010</span></span>                                                     |
| <span data-ttu-id="cb8d1-269">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="cb8d1-269">Classes used in</span></span>        | [<span data-ttu-id="cb8d1-270">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="cb8d1-270">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



 

 





