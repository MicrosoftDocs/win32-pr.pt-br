---
title: MSMQ-Authenticate atributo
description: Indica se a fila aceita somente mensagens autenticadas.
ms.assetid: f03316e3-daae-4d1e-b135-8b4c3c2765b2
ms.tgt_platform: multiple
keywords:
- Esquema de MSMQ-Authenticate do atributo AD
- Esquema de AD do atributo mSMQAuthenticate
topic_type:
- apiref
api_name:
- MSMQ-Authenticate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5a2d3744a01834cde181f5cfcf3804a0c765415
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104500067"
---
# <a name="msmq-authenticate-attribute"></a><span data-ttu-id="9de50-105">MSMQ-Authenticate atributo</span><span class="sxs-lookup"><span data-stu-id="9de50-105">MSMQ-Authenticate attribute</span></span>

<span data-ttu-id="9de50-106">Indica se a fila aceita somente mensagens autenticadas.</span><span class="sxs-lookup"><span data-stu-id="9de50-106">Indicates whether the queue accepts only authenticated messages.</span></span>



| <span data-ttu-id="9de50-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="9de50-107">Entry</span></span> | <span data-ttu-id="9de50-108">Valor</span><span class="sxs-lookup"><span data-stu-id="9de50-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="9de50-109">CN</span><span class="sxs-lookup"><span data-stu-id="9de50-109">CN</span></span>                | <span data-ttu-id="9de50-110">MSMQ-Authenticate</span><span class="sxs-lookup"><span data-stu-id="9de50-110">MSMQ-Authenticate</span></span>                    |
| <span data-ttu-id="9de50-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9de50-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9de50-112">mSMQAuthenticate</span><span class="sxs-lookup"><span data-stu-id="9de50-112">mSMQAuthenticate</span></span>                     |
| <span data-ttu-id="9de50-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="9de50-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="9de50-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="9de50-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="9de50-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="9de50-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="9de50-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9de50-116">Attribute-Id</span></span>      | <span data-ttu-id="9de50-117">1.2.840.113556.1.4.923</span><span class="sxs-lookup"><span data-stu-id="9de50-117">1.2.840.113556.1.4.923</span></span>               |
| <span data-ttu-id="9de50-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9de50-118">System-Id-Guid</span></span>    | <span data-ttu-id="9de50-119">9a0dc326-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="9de50-119">9a0dc326-c100-11d1-bbc5-0080c76670c0</span></span> |
| <span data-ttu-id="9de50-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="9de50-120">Syntax</span></span>            | [<span data-ttu-id="9de50-121">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="9de50-121">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="9de50-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="9de50-122">Implementations</span></span>

-   [<span data-ttu-id="9de50-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9de50-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9de50-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9de50-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9de50-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9de50-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9de50-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9de50-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9de50-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9de50-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9de50-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9de50-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9de50-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9de50-129">Windows 2000 Server</span></span>



| <span data-ttu-id="9de50-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="9de50-130">Entry</span></span> | <span data-ttu-id="9de50-131">Valor</span><span class="sxs-lookup"><span data-stu-id="9de50-131">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9de50-132">ID do link</span><span class="sxs-lookup"><span data-stu-id="9de50-132">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9de50-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9de50-133">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9de50-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="9de50-134">System-Only</span></span>            | <span data-ttu-id="9de50-135">Falso</span><span class="sxs-lookup"><span data-stu-id="9de50-135">False</span></span>                                        |
| <span data-ttu-id="9de50-136">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9de50-136">Is-Single-Valued</span></span>       | <span data-ttu-id="9de50-137">True</span><span class="sxs-lookup"><span data-stu-id="9de50-137">True</span></span>                                         |
| <span data-ttu-id="9de50-138">É indexado</span><span class="sxs-lookup"><span data-stu-id="9de50-138">Is Indexed</span></span>             | <span data-ttu-id="9de50-139">Falso</span><span class="sxs-lookup"><span data-stu-id="9de50-139">False</span></span>                                        |
| <span data-ttu-id="9de50-140">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9de50-140">In Global Catalog</span></span>      | <span data-ttu-id="9de50-141">True</span><span class="sxs-lookup"><span data-stu-id="9de50-141">True</span></span>                                         |
| <span data-ttu-id="9de50-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9de50-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="9de50-143">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9de50-143">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9de50-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9de50-144">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9de50-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9de50-145">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9de50-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9de50-146">Search-Flags</span></span>           | <span data-ttu-id="9de50-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9de50-147">0x00000000</span></span>                                   |
| <span data-ttu-id="9de50-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9de50-148">System-Flags</span></span>           | <span data-ttu-id="9de50-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9de50-149">0x00000010</span></span>                                   |
| <span data-ttu-id="9de50-150">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9de50-150">Classes used in</span></span>        | [<span data-ttu-id="9de50-151">**Fila MSMQ**</span><span class="sxs-lookup"><span data-stu-id="9de50-151">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9de50-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9de50-152">Windows Server 2003</span></span>



| <span data-ttu-id="9de50-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="9de50-153">Entry</span></span> | <span data-ttu-id="9de50-154">Valor</span><span class="sxs-lookup"><span data-stu-id="9de50-154">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9de50-155">ID do link</span><span class="sxs-lookup"><span data-stu-id="9de50-155">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9de50-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9de50-156">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9de50-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="9de50-157">System-Only</span></span>            | <span data-ttu-id="9de50-158">Falso</span><span class="sxs-lookup"><span data-stu-id="9de50-158">False</span></span>                                        |
| <span data-ttu-id="9de50-159">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9de50-159">Is-Single-Valued</span></span>       | <span data-ttu-id="9de50-160">True</span><span class="sxs-lookup"><span data-stu-id="9de50-160">True</span></span>                                         |
| <span data-ttu-id="9de50-161">É indexado</span><span class="sxs-lookup"><span data-stu-id="9de50-161">Is Indexed</span></span>             | <span data-ttu-id="9de50-162">Falso</span><span class="sxs-lookup"><span data-stu-id="9de50-162">False</span></span>                                        |
| <span data-ttu-id="9de50-163">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9de50-163">In Global Catalog</span></span>      | <span data-ttu-id="9de50-164">True</span><span class="sxs-lookup"><span data-stu-id="9de50-164">True</span></span>                                         |
| <span data-ttu-id="9de50-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9de50-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="9de50-166">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9de50-166">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9de50-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9de50-167">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9de50-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9de50-168">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9de50-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9de50-169">Search-Flags</span></span>           | <span data-ttu-id="9de50-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9de50-170">0x00000000</span></span>                                   |
| <span data-ttu-id="9de50-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9de50-171">System-Flags</span></span>           | <span data-ttu-id="9de50-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9de50-172">0x00000010</span></span>                                   |
| <span data-ttu-id="9de50-173">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9de50-173">Classes used in</span></span>        | [<span data-ttu-id="9de50-174">**Fila MSMQ**</span><span class="sxs-lookup"><span data-stu-id="9de50-174">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9de50-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9de50-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9de50-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="9de50-176">Entry</span></span> | <span data-ttu-id="9de50-177">Valor</span><span class="sxs-lookup"><span data-stu-id="9de50-177">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9de50-178">ID do link</span><span class="sxs-lookup"><span data-stu-id="9de50-178">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9de50-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9de50-179">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9de50-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="9de50-180">System-Only</span></span>            | <span data-ttu-id="9de50-181">Falso</span><span class="sxs-lookup"><span data-stu-id="9de50-181">False</span></span>                                        |
| <span data-ttu-id="9de50-182">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9de50-182">Is-Single-Valued</span></span>       | <span data-ttu-id="9de50-183">True</span><span class="sxs-lookup"><span data-stu-id="9de50-183">True</span></span>                                         |
| <span data-ttu-id="9de50-184">É indexado</span><span class="sxs-lookup"><span data-stu-id="9de50-184">Is Indexed</span></span>             | <span data-ttu-id="9de50-185">Falso</span><span class="sxs-lookup"><span data-stu-id="9de50-185">False</span></span>                                        |
| <span data-ttu-id="9de50-186">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9de50-186">In Global Catalog</span></span>      | <span data-ttu-id="9de50-187">True</span><span class="sxs-lookup"><span data-stu-id="9de50-187">True</span></span>                                         |
| <span data-ttu-id="9de50-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9de50-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="9de50-189">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9de50-189">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9de50-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9de50-190">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9de50-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9de50-191">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9de50-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9de50-192">Search-Flags</span></span>           | <span data-ttu-id="9de50-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9de50-193">0x00000000</span></span>                                   |
| <span data-ttu-id="9de50-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9de50-194">System-Flags</span></span>           | <span data-ttu-id="9de50-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9de50-195">0x00000010</span></span>                                   |
| <span data-ttu-id="9de50-196">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9de50-196">Classes used in</span></span>        | [<span data-ttu-id="9de50-197">**Fila MSMQ**</span><span class="sxs-lookup"><span data-stu-id="9de50-197">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9de50-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9de50-198">Windows Server 2008</span></span>



| <span data-ttu-id="9de50-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="9de50-199">Entry</span></span> | <span data-ttu-id="9de50-200">Valor</span><span class="sxs-lookup"><span data-stu-id="9de50-200">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9de50-201">ID do link</span><span class="sxs-lookup"><span data-stu-id="9de50-201">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9de50-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9de50-202">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9de50-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="9de50-203">System-Only</span></span>            | <span data-ttu-id="9de50-204">Falso</span><span class="sxs-lookup"><span data-stu-id="9de50-204">False</span></span>                                        |
| <span data-ttu-id="9de50-205">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9de50-205">Is-Single-Valued</span></span>       | <span data-ttu-id="9de50-206">True</span><span class="sxs-lookup"><span data-stu-id="9de50-206">True</span></span>                                         |
| <span data-ttu-id="9de50-207">É indexado</span><span class="sxs-lookup"><span data-stu-id="9de50-207">Is Indexed</span></span>             | <span data-ttu-id="9de50-208">Falso</span><span class="sxs-lookup"><span data-stu-id="9de50-208">False</span></span>                                        |
| <span data-ttu-id="9de50-209">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9de50-209">In Global Catalog</span></span>      | <span data-ttu-id="9de50-210">True</span><span class="sxs-lookup"><span data-stu-id="9de50-210">True</span></span>                                         |
| <span data-ttu-id="9de50-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9de50-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="9de50-212">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9de50-212">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9de50-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9de50-213">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9de50-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9de50-214">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9de50-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9de50-215">Search-Flags</span></span>           | <span data-ttu-id="9de50-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9de50-216">0x00000000</span></span>                                   |
| <span data-ttu-id="9de50-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9de50-217">System-Flags</span></span>           | <span data-ttu-id="9de50-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9de50-218">0x00000010</span></span>                                   |
| <span data-ttu-id="9de50-219">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9de50-219">Classes used in</span></span>        | [<span data-ttu-id="9de50-220">**Fila MSMQ**</span><span class="sxs-lookup"><span data-stu-id="9de50-220">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9de50-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9de50-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9de50-222">Entrada</span><span class="sxs-lookup"><span data-stu-id="9de50-222">Entry</span></span> | <span data-ttu-id="9de50-223">Valor</span><span class="sxs-lookup"><span data-stu-id="9de50-223">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9de50-224">ID do link</span><span class="sxs-lookup"><span data-stu-id="9de50-224">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9de50-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9de50-225">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9de50-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="9de50-226">System-Only</span></span>            | <span data-ttu-id="9de50-227">Falso</span><span class="sxs-lookup"><span data-stu-id="9de50-227">False</span></span>                                        |
| <span data-ttu-id="9de50-228">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9de50-228">Is-Single-Valued</span></span>       | <span data-ttu-id="9de50-229">True</span><span class="sxs-lookup"><span data-stu-id="9de50-229">True</span></span>                                         |
| <span data-ttu-id="9de50-230">É indexado</span><span class="sxs-lookup"><span data-stu-id="9de50-230">Is Indexed</span></span>             | <span data-ttu-id="9de50-231">Falso</span><span class="sxs-lookup"><span data-stu-id="9de50-231">False</span></span>                                        |
| <span data-ttu-id="9de50-232">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9de50-232">In Global Catalog</span></span>      | <span data-ttu-id="9de50-233">True</span><span class="sxs-lookup"><span data-stu-id="9de50-233">True</span></span>                                         |
| <span data-ttu-id="9de50-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9de50-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="9de50-235">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9de50-235">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9de50-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9de50-236">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9de50-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9de50-237">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9de50-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9de50-238">Search-Flags</span></span>           | <span data-ttu-id="9de50-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9de50-239">0x00000000</span></span>                                   |
| <span data-ttu-id="9de50-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9de50-240">System-Flags</span></span>           | <span data-ttu-id="9de50-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9de50-241">0x00000010</span></span>                                   |
| <span data-ttu-id="9de50-242">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9de50-242">Classes used in</span></span>        | [<span data-ttu-id="9de50-243">**Fila MSMQ**</span><span class="sxs-lookup"><span data-stu-id="9de50-243">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9de50-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9de50-244">Windows Server 2012</span></span>



| <span data-ttu-id="9de50-245">Entrada</span><span class="sxs-lookup"><span data-stu-id="9de50-245">Entry</span></span> | <span data-ttu-id="9de50-246">Valor</span><span class="sxs-lookup"><span data-stu-id="9de50-246">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9de50-247">ID do link</span><span class="sxs-lookup"><span data-stu-id="9de50-247">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9de50-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9de50-248">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9de50-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="9de50-249">System-Only</span></span>            | <span data-ttu-id="9de50-250">Falso</span><span class="sxs-lookup"><span data-stu-id="9de50-250">False</span></span>                                        |
| <span data-ttu-id="9de50-251">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9de50-251">Is-Single-Valued</span></span>       | <span data-ttu-id="9de50-252">True</span><span class="sxs-lookup"><span data-stu-id="9de50-252">True</span></span>                                         |
| <span data-ttu-id="9de50-253">É indexado</span><span class="sxs-lookup"><span data-stu-id="9de50-253">Is Indexed</span></span>             | <span data-ttu-id="9de50-254">Falso</span><span class="sxs-lookup"><span data-stu-id="9de50-254">False</span></span>                                        |
| <span data-ttu-id="9de50-255">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9de50-255">In Global Catalog</span></span>      | <span data-ttu-id="9de50-256">True</span><span class="sxs-lookup"><span data-stu-id="9de50-256">True</span></span>                                         |
| <span data-ttu-id="9de50-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9de50-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="9de50-258">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9de50-258">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9de50-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9de50-259">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9de50-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9de50-260">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9de50-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9de50-261">Search-Flags</span></span>           | <span data-ttu-id="9de50-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9de50-262">0x00000000</span></span>                                   |
| <span data-ttu-id="9de50-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9de50-263">System-Flags</span></span>           | <span data-ttu-id="9de50-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9de50-264">0x00000010</span></span>                                   |
| <span data-ttu-id="9de50-265">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9de50-265">Classes used in</span></span>        | [<span data-ttu-id="9de50-266">**Fila MSMQ**</span><span class="sxs-lookup"><span data-stu-id="9de50-266">**MSMQ-Queue**</span></span>](c-msmqqueue.md)<br/> |



 

 





