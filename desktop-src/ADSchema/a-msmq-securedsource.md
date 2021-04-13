---
title: Atributo de origem protegido pelo MSMQ
description: Isso faz parte de um objeto MSMQ, ele é definido chamando-se API para MQCreateQueue ou MQSetProperties. Ele controla se o MSMQ aceita mensagens somente de uma fonte protegida (por exemplo, HTTPS) para essa fila.
ms.assetid: 780d164f-c7fa-4c65-b46e-3a67ead92163
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo de origem protegido pelo MSMQ
- Esquema de MSMQ-SecuredSource do atributo AD
topic_type:
- apiref
api_name:
- MSMQ-Secured-Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5dd005cedcd650aa0604a85e78a46d10f1e01b0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104499978"
---
# <a name="msmq-secured-source-attribute"></a><span data-ttu-id="6ee1e-106">Atributo de origem protegido pelo MSMQ</span><span class="sxs-lookup"><span data-stu-id="6ee1e-106">MSMQ-Secured-Source attribute</span></span>

<span data-ttu-id="6ee1e-107">Isso faz parte de um objeto MSMQ, ele é definido chamando-se API para MQCreateQueue ou MQSetProperties.</span><span class="sxs-lookup"><span data-stu-id="6ee1e-107">This is part of an MSMQ object, it is set by calling API to MQCreateQueue or MQSetProperties.</span></span> <span data-ttu-id="6ee1e-108">Ele controla se o MSMQ aceita mensagens somente de uma fonte protegida (por exemplo, HTTPS) para essa fila.</span><span class="sxs-lookup"><span data-stu-id="6ee1e-108">It controls whether MSMQ accepts messages only from a secured source (for example, https) for this queue.</span></span>



| <span data-ttu-id="6ee1e-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="6ee1e-109">Entry</span></span> | <span data-ttu-id="6ee1e-110">Valor</span><span class="sxs-lookup"><span data-stu-id="6ee1e-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="6ee1e-111">CN</span><span class="sxs-lookup"><span data-stu-id="6ee1e-111">CN</span></span>                | <span data-ttu-id="6ee1e-112">Fonte protegida pelo MSMQ</span><span class="sxs-lookup"><span data-stu-id="6ee1e-112">MSMQ-Secured-Source</span></span>                  |
| <span data-ttu-id="6ee1e-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6ee1e-113">Ldap-Display-Name</span></span> | <span data-ttu-id="6ee1e-114">MSMQ-SecuredSource</span><span class="sxs-lookup"><span data-stu-id="6ee1e-114">MSMQ-SecuredSource</span></span>                   |
| <span data-ttu-id="6ee1e-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="6ee1e-115">Size</span></span>              | <span data-ttu-id="6ee1e-116">4 bytes</span><span class="sxs-lookup"><span data-stu-id="6ee1e-116">4 bytes</span></span>                              |
| <span data-ttu-id="6ee1e-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="6ee1e-117">Update Privilege</span></span>  | <span data-ttu-id="6ee1e-118">O proprietário da fila.</span><span class="sxs-lookup"><span data-stu-id="6ee1e-118">The queue owner.</span></span>                     |
| <span data-ttu-id="6ee1e-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="6ee1e-119">Update Frequency</span></span>  | <span data-ttu-id="6ee1e-120">Quando uma fila é criada.</span><span class="sxs-lookup"><span data-stu-id="6ee1e-120">When a queue is created.</span></span>             |
| <span data-ttu-id="6ee1e-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6ee1e-121">Attribute-Id</span></span>      | <span data-ttu-id="6ee1e-122">1.2.840.113556.1.4.1713</span><span class="sxs-lookup"><span data-stu-id="6ee1e-122">1.2.840.113556.1.4.1713</span></span>              |
| <span data-ttu-id="6ee1e-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6ee1e-123">System-Id-Guid</span></span>    | <span data-ttu-id="6ee1e-124">8bf0221b-7a06-4d63-91f0-1499941813d3</span><span class="sxs-lookup"><span data-stu-id="6ee1e-124">8bf0221b-7a06-4d63-91f0-1499941813d3</span></span> |
| <span data-ttu-id="6ee1e-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ee1e-125">Syntax</span></span>            | [<span data-ttu-id="6ee1e-126">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="6ee1e-126">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="6ee1e-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="6ee1e-127">Implementations</span></span>

-   [<span data-ttu-id="6ee1e-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6ee1e-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6ee1e-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6ee1e-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6ee1e-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6ee1e-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6ee1e-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6ee1e-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6ee1e-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6ee1e-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="6ee1e-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6ee1e-133">Windows Server 2003</span></span>



| <span data-ttu-id="6ee1e-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="6ee1e-134">Entry</span></span> | <span data-ttu-id="6ee1e-135">Valor</span><span class="sxs-lookup"><span data-stu-id="6ee1e-135">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6ee1e-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="6ee1e-136">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6ee1e-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ee1e-137">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6ee1e-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ee1e-138">System-Only</span></span>            | <span data-ttu-id="6ee1e-139">Falso</span><span class="sxs-lookup"><span data-stu-id="6ee1e-139">False</span></span>                                        |
| <span data-ttu-id="6ee1e-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6ee1e-140">Is-Single-Valued</span></span>       | <span data-ttu-id="6ee1e-141">True</span><span class="sxs-lookup"><span data-stu-id="6ee1e-141">True</span></span>                                         |
| <span data-ttu-id="6ee1e-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="6ee1e-142">Is Indexed</span></span>             | <span data-ttu-id="6ee1e-143">Falso</span><span class="sxs-lookup"><span data-stu-id="6ee1e-143">False</span></span>                                        |
| <span data-ttu-id="6ee1e-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6ee1e-144">In Global Catalog</span></span>      | <span data-ttu-id="6ee1e-145">True</span><span class="sxs-lookup"><span data-stu-id="6ee1e-145">True</span></span>                                         |
| <span data-ttu-id="6ee1e-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6ee1e-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ee1e-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6ee1e-147">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6ee1e-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ee1e-148">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6ee1e-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ee1e-149">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6ee1e-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ee1e-150">Search-Flags</span></span>           | <span data-ttu-id="6ee1e-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6ee1e-151">0x00000000</span></span>                                   |
| <span data-ttu-id="6ee1e-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ee1e-152">System-Flags</span></span>           | <span data-ttu-id="6ee1e-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ee1e-153">0x00000010</span></span>                                   |
| <span data-ttu-id="6ee1e-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6ee1e-154">Classes used in</span></span>        | [<span data-ttu-id="6ee1e-155">**Fila MSMQ**</span><span class="sxs-lookup"><span data-stu-id="6ee1e-155">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6ee1e-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6ee1e-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6ee1e-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="6ee1e-157">Entry</span></span> | <span data-ttu-id="6ee1e-158">Valor</span><span class="sxs-lookup"><span data-stu-id="6ee1e-158">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6ee1e-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="6ee1e-159">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6ee1e-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ee1e-160">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6ee1e-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ee1e-161">System-Only</span></span>            | <span data-ttu-id="6ee1e-162">Falso</span><span class="sxs-lookup"><span data-stu-id="6ee1e-162">False</span></span>                                        |
| <span data-ttu-id="6ee1e-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6ee1e-163">Is-Single-Valued</span></span>       | <span data-ttu-id="6ee1e-164">True</span><span class="sxs-lookup"><span data-stu-id="6ee1e-164">True</span></span>                                         |
| <span data-ttu-id="6ee1e-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="6ee1e-165">Is Indexed</span></span>             | <span data-ttu-id="6ee1e-166">Falso</span><span class="sxs-lookup"><span data-stu-id="6ee1e-166">False</span></span>                                        |
| <span data-ttu-id="6ee1e-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6ee1e-167">In Global Catalog</span></span>      | <span data-ttu-id="6ee1e-168">True</span><span class="sxs-lookup"><span data-stu-id="6ee1e-168">True</span></span>                                         |
| <span data-ttu-id="6ee1e-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6ee1e-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ee1e-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6ee1e-170">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6ee1e-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ee1e-171">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6ee1e-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ee1e-172">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6ee1e-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ee1e-173">Search-Flags</span></span>           | <span data-ttu-id="6ee1e-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6ee1e-174">0x00000000</span></span>                                   |
| <span data-ttu-id="6ee1e-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ee1e-175">System-Flags</span></span>           | <span data-ttu-id="6ee1e-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ee1e-176">0x00000010</span></span>                                   |
| <span data-ttu-id="6ee1e-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6ee1e-177">Classes used in</span></span>        | [<span data-ttu-id="6ee1e-178">**Fila MSMQ**</span><span class="sxs-lookup"><span data-stu-id="6ee1e-178">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6ee1e-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ee1e-179">Windows Server 2008</span></span>



| <span data-ttu-id="6ee1e-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="6ee1e-180">Entry</span></span> | <span data-ttu-id="6ee1e-181">Valor</span><span class="sxs-lookup"><span data-stu-id="6ee1e-181">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6ee1e-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="6ee1e-182">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6ee1e-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ee1e-183">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6ee1e-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ee1e-184">System-Only</span></span>            | <span data-ttu-id="6ee1e-185">Falso</span><span class="sxs-lookup"><span data-stu-id="6ee1e-185">False</span></span>                                        |
| <span data-ttu-id="6ee1e-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6ee1e-186">Is-Single-Valued</span></span>       | <span data-ttu-id="6ee1e-187">True</span><span class="sxs-lookup"><span data-stu-id="6ee1e-187">True</span></span>                                         |
| <span data-ttu-id="6ee1e-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="6ee1e-188">Is Indexed</span></span>             | <span data-ttu-id="6ee1e-189">Falso</span><span class="sxs-lookup"><span data-stu-id="6ee1e-189">False</span></span>                                        |
| <span data-ttu-id="6ee1e-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6ee1e-190">In Global Catalog</span></span>      | <span data-ttu-id="6ee1e-191">True</span><span class="sxs-lookup"><span data-stu-id="6ee1e-191">True</span></span>                                         |
| <span data-ttu-id="6ee1e-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6ee1e-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ee1e-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6ee1e-193">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6ee1e-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ee1e-194">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6ee1e-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ee1e-195">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6ee1e-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ee1e-196">Search-Flags</span></span>           | <span data-ttu-id="6ee1e-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6ee1e-197">0x00000000</span></span>                                   |
| <span data-ttu-id="6ee1e-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ee1e-198">System-Flags</span></span>           | <span data-ttu-id="6ee1e-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ee1e-199">0x00000010</span></span>                                   |
| <span data-ttu-id="6ee1e-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6ee1e-200">Classes used in</span></span>        | [<span data-ttu-id="6ee1e-201">**Fila MSMQ**</span><span class="sxs-lookup"><span data-stu-id="6ee1e-201">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6ee1e-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6ee1e-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6ee1e-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="6ee1e-203">Entry</span></span> | <span data-ttu-id="6ee1e-204">Valor</span><span class="sxs-lookup"><span data-stu-id="6ee1e-204">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6ee1e-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="6ee1e-205">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6ee1e-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ee1e-206">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6ee1e-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ee1e-207">System-Only</span></span>            | <span data-ttu-id="6ee1e-208">Falso</span><span class="sxs-lookup"><span data-stu-id="6ee1e-208">False</span></span>                                        |
| <span data-ttu-id="6ee1e-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6ee1e-209">Is-Single-Valued</span></span>       | <span data-ttu-id="6ee1e-210">True</span><span class="sxs-lookup"><span data-stu-id="6ee1e-210">True</span></span>                                         |
| <span data-ttu-id="6ee1e-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="6ee1e-211">Is Indexed</span></span>             | <span data-ttu-id="6ee1e-212">Falso</span><span class="sxs-lookup"><span data-stu-id="6ee1e-212">False</span></span>                                        |
| <span data-ttu-id="6ee1e-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6ee1e-213">In Global Catalog</span></span>      | <span data-ttu-id="6ee1e-214">True</span><span class="sxs-lookup"><span data-stu-id="6ee1e-214">True</span></span>                                         |
| <span data-ttu-id="6ee1e-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6ee1e-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ee1e-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6ee1e-216">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6ee1e-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ee1e-217">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6ee1e-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ee1e-218">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6ee1e-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ee1e-219">Search-Flags</span></span>           | <span data-ttu-id="6ee1e-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6ee1e-220">0x00000000</span></span>                                   |
| <span data-ttu-id="6ee1e-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ee1e-221">System-Flags</span></span>           | <span data-ttu-id="6ee1e-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ee1e-222">0x00000010</span></span>                                   |
| <span data-ttu-id="6ee1e-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6ee1e-223">Classes used in</span></span>        | [<span data-ttu-id="6ee1e-224">**Fila MSMQ**</span><span class="sxs-lookup"><span data-stu-id="6ee1e-224">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6ee1e-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6ee1e-225">Windows Server 2012</span></span>



| <span data-ttu-id="6ee1e-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="6ee1e-226">Entry</span></span> | <span data-ttu-id="6ee1e-227">Valor</span><span class="sxs-lookup"><span data-stu-id="6ee1e-227">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="6ee1e-228">ID do link</span><span class="sxs-lookup"><span data-stu-id="6ee1e-228">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="6ee1e-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ee1e-229">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="6ee1e-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ee1e-230">System-Only</span></span>            | <span data-ttu-id="6ee1e-231">Falso</span><span class="sxs-lookup"><span data-stu-id="6ee1e-231">False</span></span>                                        |
| <span data-ttu-id="6ee1e-232">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6ee1e-232">Is-Single-Valued</span></span>       | <span data-ttu-id="6ee1e-233">True</span><span class="sxs-lookup"><span data-stu-id="6ee1e-233">True</span></span>                                         |
| <span data-ttu-id="6ee1e-234">É indexado</span><span class="sxs-lookup"><span data-stu-id="6ee1e-234">Is Indexed</span></span>             | <span data-ttu-id="6ee1e-235">Falso</span><span class="sxs-lookup"><span data-stu-id="6ee1e-235">False</span></span>                                        |
| <span data-ttu-id="6ee1e-236">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6ee1e-236">In Global Catalog</span></span>      | <span data-ttu-id="6ee1e-237">True</span><span class="sxs-lookup"><span data-stu-id="6ee1e-237">True</span></span>                                         |
| <span data-ttu-id="6ee1e-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6ee1e-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ee1e-239">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6ee1e-239">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="6ee1e-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ee1e-240">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="6ee1e-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ee1e-241">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="6ee1e-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ee1e-242">Search-Flags</span></span>           | <span data-ttu-id="6ee1e-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6ee1e-243">0x00000000</span></span>                                   |
| <span data-ttu-id="6ee1e-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ee1e-244">System-Flags</span></span>           | <span data-ttu-id="6ee1e-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ee1e-245">0x00000010</span></span>                                   |
| <span data-ttu-id="6ee1e-246">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6ee1e-246">Classes used in</span></span>        | [<span data-ttu-id="6ee1e-247">**Fila MSMQ**</span><span class="sxs-lookup"><span data-stu-id="6ee1e-247">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



 

 





