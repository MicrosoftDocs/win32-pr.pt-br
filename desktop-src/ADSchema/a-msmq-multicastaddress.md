---
title: Atributo MSMQ-multicast-address
description: Isso faz parte de um objeto MSMQ, ele é definido chamando-se API para MQCreateQueue ou MQSetProperties. Ele controla se o MSMQ aceitará mensagens de um endereço multicast.
ms.assetid: 65622cc9-81d9-42c6-b208-cac703f32244
ms.tgt_platform: multiple
keywords:
- MSMQ-multicast – atributo de endereço do AD Schema
- Esquema de MSMQ-MulticastAddress do atributo AD
topic_type:
- apiref
api_name:
- MSMQ-Multicast-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a1b90543c40e22d8dd5fdc2b3e5195bd9382357
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104499979"
---
# <a name="msmq-multicast-address-attribute"></a><span data-ttu-id="d9e98-106">Atributo MSMQ-multicast-address</span><span class="sxs-lookup"><span data-stu-id="d9e98-106">MSMQ-Multicast-Address attribute</span></span>

<span data-ttu-id="d9e98-107">Isso faz parte de um objeto MSMQ, ele é definido chamando-se API para MQCreateQueue ou MQSetProperties.</span><span class="sxs-lookup"><span data-stu-id="d9e98-107">This is part of an MSMQ object, it is set by calling API to MQCreateQueue or MQSetProperties.</span></span> <span data-ttu-id="d9e98-108">Ele controla se o MSMQ aceitará mensagens de um endereço multicast.</span><span class="sxs-lookup"><span data-stu-id="d9e98-108">It controls whether MSMQ will accept messages from a multicast address.</span></span>



| <span data-ttu-id="d9e98-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="d9e98-109">Entry</span></span> | <span data-ttu-id="d9e98-110">Valor</span><span class="sxs-lookup"><span data-stu-id="d9e98-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="d9e98-111">CN</span><span class="sxs-lookup"><span data-stu-id="d9e98-111">CN</span></span>                | <span data-ttu-id="d9e98-112">MSMQ-endereço de multicast</span><span class="sxs-lookup"><span data-stu-id="d9e98-112">MSMQ-Multicast-Address</span></span>                      |
| <span data-ttu-id="d9e98-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d9e98-113">Ldap-Display-Name</span></span> | <span data-ttu-id="d9e98-114">MSMQ-MulticastAddress</span><span class="sxs-lookup"><span data-stu-id="d9e98-114">MSMQ-MulticastAddress</span></span>                       |
| <span data-ttu-id="d9e98-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="d9e98-115">Size</span></span>              | <span data-ttu-id="d9e98-116">4 bytes</span><span class="sxs-lookup"><span data-stu-id="d9e98-116">4 bytes</span></span>                                     |
| <span data-ttu-id="d9e98-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="d9e98-117">Update Privilege</span></span>  | <span data-ttu-id="d9e98-118">O proprietário da fila.</span><span class="sxs-lookup"><span data-stu-id="d9e98-118">The queue owner.</span></span>                            |
| <span data-ttu-id="d9e98-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="d9e98-119">Update Frequency</span></span>  | <span data-ttu-id="d9e98-120">Quando uma fila é criada.</span><span class="sxs-lookup"><span data-stu-id="d9e98-120">When a queue is created.</span></span>                    |
| <span data-ttu-id="d9e98-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d9e98-121">Attribute-Id</span></span>      | <span data-ttu-id="d9e98-122">1.2.840.113556.1.4.1714</span><span class="sxs-lookup"><span data-stu-id="d9e98-122">1.2.840.113556.1.4.1714</span></span>                     |
| <span data-ttu-id="d9e98-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d9e98-123">System-Id-Guid</span></span>    | <span data-ttu-id="d9e98-124">1d2f4412-f10d-4337-9b48-6e5b125cd265</span><span class="sxs-lookup"><span data-stu-id="d9e98-124">1d2f4412-f10d-4337-9b48-6e5b125cd265</span></span>        |
| <span data-ttu-id="d9e98-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9e98-125">Syntax</span></span>            | [<span data-ttu-id="d9e98-126">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="d9e98-126">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="d9e98-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="d9e98-127">Implementations</span></span>

-   [<span data-ttu-id="d9e98-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d9e98-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d9e98-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d9e98-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d9e98-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d9e98-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d9e98-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d9e98-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d9e98-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d9e98-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="d9e98-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d9e98-133">Windows Server 2003</span></span>



| <span data-ttu-id="d9e98-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="d9e98-134">Entry</span></span> | <span data-ttu-id="d9e98-135">Valor</span><span class="sxs-lookup"><span data-stu-id="d9e98-135">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="d9e98-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="d9e98-136">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="d9e98-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d9e98-137">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="d9e98-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="d9e98-138">System-Only</span></span>            | <span data-ttu-id="d9e98-139">Falso</span><span class="sxs-lookup"><span data-stu-id="d9e98-139">False</span></span>                                        |
| <span data-ttu-id="d9e98-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d9e98-140">Is-Single-Valued</span></span>       | <span data-ttu-id="d9e98-141">True</span><span class="sxs-lookup"><span data-stu-id="d9e98-141">True</span></span>                                         |
| <span data-ttu-id="d9e98-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="d9e98-142">Is Indexed</span></span>             | <span data-ttu-id="d9e98-143">Falso</span><span class="sxs-lookup"><span data-stu-id="d9e98-143">False</span></span>                                        |
| <span data-ttu-id="d9e98-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d9e98-144">In Global Catalog</span></span>      | <span data-ttu-id="d9e98-145">True</span><span class="sxs-lookup"><span data-stu-id="d9e98-145">True</span></span>                                         |
| <span data-ttu-id="d9e98-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d9e98-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="d9e98-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d9e98-147">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="d9e98-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d9e98-148">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="d9e98-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d9e98-149">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="d9e98-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d9e98-150">Search-Flags</span></span>           | <span data-ttu-id="d9e98-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d9e98-151">0x00000000</span></span>                                   |
| <span data-ttu-id="d9e98-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d9e98-152">System-Flags</span></span>           | <span data-ttu-id="d9e98-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d9e98-153">0x00000010</span></span>                                   |
| <span data-ttu-id="d9e98-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d9e98-154">Classes used in</span></span>        | [<span data-ttu-id="d9e98-155">**Fila MSMQ**</span><span class="sxs-lookup"><span data-stu-id="d9e98-155">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d9e98-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d9e98-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d9e98-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="d9e98-157">Entry</span></span> | <span data-ttu-id="d9e98-158">Valor</span><span class="sxs-lookup"><span data-stu-id="d9e98-158">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="d9e98-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="d9e98-159">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="d9e98-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d9e98-160">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="d9e98-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="d9e98-161">System-Only</span></span>            | <span data-ttu-id="d9e98-162">Falso</span><span class="sxs-lookup"><span data-stu-id="d9e98-162">False</span></span>                                        |
| <span data-ttu-id="d9e98-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d9e98-163">Is-Single-Valued</span></span>       | <span data-ttu-id="d9e98-164">True</span><span class="sxs-lookup"><span data-stu-id="d9e98-164">True</span></span>                                         |
| <span data-ttu-id="d9e98-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="d9e98-165">Is Indexed</span></span>             | <span data-ttu-id="d9e98-166">Falso</span><span class="sxs-lookup"><span data-stu-id="d9e98-166">False</span></span>                                        |
| <span data-ttu-id="d9e98-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d9e98-167">In Global Catalog</span></span>      | <span data-ttu-id="d9e98-168">True</span><span class="sxs-lookup"><span data-stu-id="d9e98-168">True</span></span>                                         |
| <span data-ttu-id="d9e98-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d9e98-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="d9e98-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d9e98-170">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="d9e98-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d9e98-171">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="d9e98-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d9e98-172">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="d9e98-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d9e98-173">Search-Flags</span></span>           | <span data-ttu-id="d9e98-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d9e98-174">0x00000000</span></span>                                   |
| <span data-ttu-id="d9e98-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d9e98-175">System-Flags</span></span>           | <span data-ttu-id="d9e98-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d9e98-176">0x00000010</span></span>                                   |
| <span data-ttu-id="d9e98-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d9e98-177">Classes used in</span></span>        | [<span data-ttu-id="d9e98-178">**Fila MSMQ**</span><span class="sxs-lookup"><span data-stu-id="d9e98-178">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d9e98-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d9e98-179">Windows Server 2008</span></span>



| <span data-ttu-id="d9e98-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="d9e98-180">Entry</span></span> | <span data-ttu-id="d9e98-181">Valor</span><span class="sxs-lookup"><span data-stu-id="d9e98-181">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="d9e98-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="d9e98-182">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="d9e98-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d9e98-183">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="d9e98-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="d9e98-184">System-Only</span></span>            | <span data-ttu-id="d9e98-185">Falso</span><span class="sxs-lookup"><span data-stu-id="d9e98-185">False</span></span>                                        |
| <span data-ttu-id="d9e98-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d9e98-186">Is-Single-Valued</span></span>       | <span data-ttu-id="d9e98-187">True</span><span class="sxs-lookup"><span data-stu-id="d9e98-187">True</span></span>                                         |
| <span data-ttu-id="d9e98-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="d9e98-188">Is Indexed</span></span>             | <span data-ttu-id="d9e98-189">Falso</span><span class="sxs-lookup"><span data-stu-id="d9e98-189">False</span></span>                                        |
| <span data-ttu-id="d9e98-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d9e98-190">In Global Catalog</span></span>      | <span data-ttu-id="d9e98-191">True</span><span class="sxs-lookup"><span data-stu-id="d9e98-191">True</span></span>                                         |
| <span data-ttu-id="d9e98-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d9e98-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="d9e98-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d9e98-193">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="d9e98-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d9e98-194">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="d9e98-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d9e98-195">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="d9e98-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d9e98-196">Search-Flags</span></span>           | <span data-ttu-id="d9e98-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d9e98-197">0x00000000</span></span>                                   |
| <span data-ttu-id="d9e98-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d9e98-198">System-Flags</span></span>           | <span data-ttu-id="d9e98-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d9e98-199">0x00000010</span></span>                                   |
| <span data-ttu-id="d9e98-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d9e98-200">Classes used in</span></span>        | [<span data-ttu-id="d9e98-201">**Fila MSMQ**</span><span class="sxs-lookup"><span data-stu-id="d9e98-201">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d9e98-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d9e98-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d9e98-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="d9e98-203">Entry</span></span> | <span data-ttu-id="d9e98-204">Valor</span><span class="sxs-lookup"><span data-stu-id="d9e98-204">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="d9e98-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="d9e98-205">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="d9e98-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d9e98-206">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="d9e98-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="d9e98-207">System-Only</span></span>            | <span data-ttu-id="d9e98-208">Falso</span><span class="sxs-lookup"><span data-stu-id="d9e98-208">False</span></span>                                        |
| <span data-ttu-id="d9e98-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d9e98-209">Is-Single-Valued</span></span>       | <span data-ttu-id="d9e98-210">True</span><span class="sxs-lookup"><span data-stu-id="d9e98-210">True</span></span>                                         |
| <span data-ttu-id="d9e98-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="d9e98-211">Is Indexed</span></span>             | <span data-ttu-id="d9e98-212">Falso</span><span class="sxs-lookup"><span data-stu-id="d9e98-212">False</span></span>                                        |
| <span data-ttu-id="d9e98-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d9e98-213">In Global Catalog</span></span>      | <span data-ttu-id="d9e98-214">True</span><span class="sxs-lookup"><span data-stu-id="d9e98-214">True</span></span>                                         |
| <span data-ttu-id="d9e98-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d9e98-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="d9e98-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d9e98-216">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="d9e98-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d9e98-217">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="d9e98-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d9e98-218">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="d9e98-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d9e98-219">Search-Flags</span></span>           | <span data-ttu-id="d9e98-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d9e98-220">0x00000000</span></span>                                   |
| <span data-ttu-id="d9e98-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d9e98-221">System-Flags</span></span>           | <span data-ttu-id="d9e98-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d9e98-222">0x00000010</span></span>                                   |
| <span data-ttu-id="d9e98-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d9e98-223">Classes used in</span></span>        | [<span data-ttu-id="d9e98-224">**Fila MSMQ**</span><span class="sxs-lookup"><span data-stu-id="d9e98-224">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d9e98-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d9e98-225">Windows Server 2012</span></span>



| <span data-ttu-id="d9e98-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="d9e98-226">Entry</span></span> | <span data-ttu-id="d9e98-227">Valor</span><span class="sxs-lookup"><span data-stu-id="d9e98-227">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="d9e98-228">ID do link</span><span class="sxs-lookup"><span data-stu-id="d9e98-228">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="d9e98-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d9e98-229">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="d9e98-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="d9e98-230">System-Only</span></span>            | <span data-ttu-id="d9e98-231">Falso</span><span class="sxs-lookup"><span data-stu-id="d9e98-231">False</span></span>                                        |
| <span data-ttu-id="d9e98-232">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d9e98-232">Is-Single-Valued</span></span>       | <span data-ttu-id="d9e98-233">True</span><span class="sxs-lookup"><span data-stu-id="d9e98-233">True</span></span>                                         |
| <span data-ttu-id="d9e98-234">É indexado</span><span class="sxs-lookup"><span data-stu-id="d9e98-234">Is Indexed</span></span>             | <span data-ttu-id="d9e98-235">Falso</span><span class="sxs-lookup"><span data-stu-id="d9e98-235">False</span></span>                                        |
| <span data-ttu-id="d9e98-236">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d9e98-236">In Global Catalog</span></span>      | <span data-ttu-id="d9e98-237">True</span><span class="sxs-lookup"><span data-stu-id="d9e98-237">True</span></span>                                         |
| <span data-ttu-id="d9e98-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d9e98-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="d9e98-239">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d9e98-239">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="d9e98-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d9e98-240">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="d9e98-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d9e98-241">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="d9e98-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d9e98-242">Search-Flags</span></span>           | <span data-ttu-id="d9e98-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d9e98-243">0x00000000</span></span>                                   |
| <span data-ttu-id="d9e98-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d9e98-244">System-Flags</span></span>           | <span data-ttu-id="d9e98-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d9e98-245">0x00000010</span></span>                                   |
| <span data-ttu-id="d9e98-246">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d9e98-246">Classes used in</span></span>        | [<span data-ttu-id="d9e98-247">**Fila MSMQ**</span><span class="sxs-lookup"><span data-stu-id="d9e98-247">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



 

 





