---
title: LSA – atributo de tempo de criação
description: O atributo LSA-Creation-time é usado para dar suporte à replicação em domínios do Windows NT 4,0.
ms.assetid: a5446cbf-aa35-4ea6-a2e0-9d0ea58edaf1
ms.tgt_platform: multiple
keywords:
- LSA – esquema de atributo de tempo de criação
- Esquema de AD do atributo lSACreationTime
topic_type:
- apiref
api_name:
- LSA-Creation-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f32092e7d71d02807f4700d381da0ce099ccaf7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104369958"
---
# <a name="lsa-creation-time-attribute"></a><span data-ttu-id="64611-105">LSA – atributo de tempo de criação</span><span class="sxs-lookup"><span data-stu-id="64611-105">LSA-Creation-Time attribute</span></span>

<span data-ttu-id="64611-106">O atributo **LSA-Creation-time** é usado para dar suporte à replicação em domínios do Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="64611-106">The **LSA-Creation-Time** attribute is used to support replication to Windows NT 4.0 domains.</span></span>



| <span data-ttu-id="64611-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="64611-107">Entry</span></span> | <span data-ttu-id="64611-108">Valor</span><span class="sxs-lookup"><span data-stu-id="64611-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="64611-109">CN</span><span class="sxs-lookup"><span data-stu-id="64611-109">CN</span></span>                | <span data-ttu-id="64611-110">LSA – tempo de criação</span><span class="sxs-lookup"><span data-stu-id="64611-110">LSA-Creation-Time</span></span>                    |
| <span data-ttu-id="64611-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="64611-111">Ldap-Display-Name</span></span> | <span data-ttu-id="64611-112">lSACreationTime</span><span class="sxs-lookup"><span data-stu-id="64611-112">lSACreationTime</span></span>                      |
| <span data-ttu-id="64611-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="64611-113">Size</span></span>              | <span data-ttu-id="64611-114">8 bytes</span><span class="sxs-lookup"><span data-stu-id="64611-114">8 bytes</span></span>                              |
| <span data-ttu-id="64611-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="64611-115">Update Privilege</span></span>  | <span data-ttu-id="64611-116">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="64611-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="64611-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="64611-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="64611-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="64611-118">Attribute-Id</span></span>      | <span data-ttu-id="64611-119">1.2.840.113556.1.4.66</span><span class="sxs-lookup"><span data-stu-id="64611-119">1.2.840.113556.1.4.66</span></span>                |
| <span data-ttu-id="64611-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="64611-120">System-Id-Guid</span></span>    | <span data-ttu-id="64611-121">bf9679ad-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="64611-121">bf9679ad-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="64611-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="64611-122">Syntax</span></span>            | [<span data-ttu-id="64611-123">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="64611-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="64611-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="64611-124">Implementations</span></span>

-   [<span data-ttu-id="64611-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="64611-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="64611-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="64611-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="64611-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="64611-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="64611-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="64611-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="64611-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="64611-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="64611-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="64611-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="64611-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="64611-131">Windows 2000 Server</span></span>



| <span data-ttu-id="64611-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="64611-132">Entry</span></span> | <span data-ttu-id="64611-133">Valor</span><span class="sxs-lookup"><span data-stu-id="64611-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="64611-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="64611-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="64611-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64611-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="64611-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="64611-136">System-Only</span></span>            | <span data-ttu-id="64611-137">Falso</span><span class="sxs-lookup"><span data-stu-id="64611-137">False</span></span>                                        |
| <span data-ttu-id="64611-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="64611-138">Is-Single-Valued</span></span>       | <span data-ttu-id="64611-139">True</span><span class="sxs-lookup"><span data-stu-id="64611-139">True</span></span>                                         |
| <span data-ttu-id="64611-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="64611-140">Is Indexed</span></span>             | <span data-ttu-id="64611-141">Falso</span><span class="sxs-lookup"><span data-stu-id="64611-141">False</span></span>                                        |
| <span data-ttu-id="64611-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="64611-142">In Global Catalog</span></span>      | <span data-ttu-id="64611-143">Falso</span><span class="sxs-lookup"><span data-stu-id="64611-143">False</span></span>                                        |
| <span data-ttu-id="64611-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64611-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="64611-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="64611-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="64611-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64611-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="64611-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64611-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="64611-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64611-148">Search-Flags</span></span>           | <span data-ttu-id="64611-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64611-149">0x00000000</span></span>                                   |
| <span data-ttu-id="64611-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64611-150">System-Flags</span></span>           | <span data-ttu-id="64611-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64611-151">0x00000010</span></span>                                   |
| <span data-ttu-id="64611-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="64611-152">Classes used in</span></span>        | [<span data-ttu-id="64611-153">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="64611-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="64611-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="64611-154">Windows Server 2003</span></span>



| <span data-ttu-id="64611-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="64611-155">Entry</span></span> | <span data-ttu-id="64611-156">Valor</span><span class="sxs-lookup"><span data-stu-id="64611-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="64611-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="64611-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="64611-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64611-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="64611-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="64611-159">System-Only</span></span>            | <span data-ttu-id="64611-160">Falso</span><span class="sxs-lookup"><span data-stu-id="64611-160">False</span></span>                                        |
| <span data-ttu-id="64611-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="64611-161">Is-Single-Valued</span></span>       | <span data-ttu-id="64611-162">True</span><span class="sxs-lookup"><span data-stu-id="64611-162">True</span></span>                                         |
| <span data-ttu-id="64611-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="64611-163">Is Indexed</span></span>             | <span data-ttu-id="64611-164">Falso</span><span class="sxs-lookup"><span data-stu-id="64611-164">False</span></span>                                        |
| <span data-ttu-id="64611-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="64611-165">In Global Catalog</span></span>      | <span data-ttu-id="64611-166">Falso</span><span class="sxs-lookup"><span data-stu-id="64611-166">False</span></span>                                        |
| <span data-ttu-id="64611-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64611-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="64611-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="64611-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="64611-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64611-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="64611-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64611-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="64611-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64611-171">Search-Flags</span></span>           | <span data-ttu-id="64611-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64611-172">0x00000000</span></span>                                   |
| <span data-ttu-id="64611-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64611-173">System-Flags</span></span>           | <span data-ttu-id="64611-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64611-174">0x00000010</span></span>                                   |
| <span data-ttu-id="64611-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="64611-175">Classes used in</span></span>        | [<span data-ttu-id="64611-176">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="64611-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="64611-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="64611-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="64611-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="64611-178">Entry</span></span> | <span data-ttu-id="64611-179">Valor</span><span class="sxs-lookup"><span data-stu-id="64611-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="64611-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="64611-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="64611-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64611-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="64611-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="64611-182">System-Only</span></span>            | <span data-ttu-id="64611-183">Falso</span><span class="sxs-lookup"><span data-stu-id="64611-183">False</span></span>                                        |
| <span data-ttu-id="64611-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="64611-184">Is-Single-Valued</span></span>       | <span data-ttu-id="64611-185">True</span><span class="sxs-lookup"><span data-stu-id="64611-185">True</span></span>                                         |
| <span data-ttu-id="64611-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="64611-186">Is Indexed</span></span>             | <span data-ttu-id="64611-187">Falso</span><span class="sxs-lookup"><span data-stu-id="64611-187">False</span></span>                                        |
| <span data-ttu-id="64611-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="64611-188">In Global Catalog</span></span>      | <span data-ttu-id="64611-189">Falso</span><span class="sxs-lookup"><span data-stu-id="64611-189">False</span></span>                                        |
| <span data-ttu-id="64611-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64611-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="64611-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="64611-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="64611-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64611-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="64611-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64611-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="64611-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64611-194">Search-Flags</span></span>           | <span data-ttu-id="64611-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64611-195">0x00000000</span></span>                                   |
| <span data-ttu-id="64611-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64611-196">System-Flags</span></span>           | <span data-ttu-id="64611-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64611-197">0x00000010</span></span>                                   |
| <span data-ttu-id="64611-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="64611-198">Classes used in</span></span>        | [<span data-ttu-id="64611-199">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="64611-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="64611-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64611-200">Windows Server 2008</span></span>



| <span data-ttu-id="64611-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="64611-201">Entry</span></span> | <span data-ttu-id="64611-202">Valor</span><span class="sxs-lookup"><span data-stu-id="64611-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="64611-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="64611-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="64611-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64611-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="64611-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="64611-205">System-Only</span></span>            | <span data-ttu-id="64611-206">Falso</span><span class="sxs-lookup"><span data-stu-id="64611-206">False</span></span>                                        |
| <span data-ttu-id="64611-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="64611-207">Is-Single-Valued</span></span>       | <span data-ttu-id="64611-208">True</span><span class="sxs-lookup"><span data-stu-id="64611-208">True</span></span>                                         |
| <span data-ttu-id="64611-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="64611-209">Is Indexed</span></span>             | <span data-ttu-id="64611-210">Falso</span><span class="sxs-lookup"><span data-stu-id="64611-210">False</span></span>                                        |
| <span data-ttu-id="64611-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="64611-211">In Global Catalog</span></span>      | <span data-ttu-id="64611-212">Falso</span><span class="sxs-lookup"><span data-stu-id="64611-212">False</span></span>                                        |
| <span data-ttu-id="64611-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64611-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="64611-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="64611-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="64611-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64611-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="64611-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64611-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="64611-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64611-217">Search-Flags</span></span>           | <span data-ttu-id="64611-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64611-218">0x00000000</span></span>                                   |
| <span data-ttu-id="64611-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64611-219">System-Flags</span></span>           | <span data-ttu-id="64611-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64611-220">0x00000010</span></span>                                   |
| <span data-ttu-id="64611-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="64611-221">Classes used in</span></span>        | [<span data-ttu-id="64611-222">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="64611-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="64611-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="64611-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="64611-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="64611-224">Entry</span></span> | <span data-ttu-id="64611-225">Valor</span><span class="sxs-lookup"><span data-stu-id="64611-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="64611-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="64611-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="64611-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64611-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="64611-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="64611-228">System-Only</span></span>            | <span data-ttu-id="64611-229">Falso</span><span class="sxs-lookup"><span data-stu-id="64611-229">False</span></span>                                        |
| <span data-ttu-id="64611-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="64611-230">Is-Single-Valued</span></span>       | <span data-ttu-id="64611-231">True</span><span class="sxs-lookup"><span data-stu-id="64611-231">True</span></span>                                         |
| <span data-ttu-id="64611-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="64611-232">Is Indexed</span></span>             | <span data-ttu-id="64611-233">Falso</span><span class="sxs-lookup"><span data-stu-id="64611-233">False</span></span>                                        |
| <span data-ttu-id="64611-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="64611-234">In Global Catalog</span></span>      | <span data-ttu-id="64611-235">Falso</span><span class="sxs-lookup"><span data-stu-id="64611-235">False</span></span>                                        |
| <span data-ttu-id="64611-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64611-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="64611-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="64611-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="64611-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64611-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="64611-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64611-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="64611-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64611-240">Search-Flags</span></span>           | <span data-ttu-id="64611-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64611-241">0x00000000</span></span>                                   |
| <span data-ttu-id="64611-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64611-242">System-Flags</span></span>           | <span data-ttu-id="64611-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64611-243">0x00000010</span></span>                                   |
| <span data-ttu-id="64611-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="64611-244">Classes used in</span></span>        | [<span data-ttu-id="64611-245">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="64611-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="64611-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="64611-246">Windows Server 2012</span></span>



| <span data-ttu-id="64611-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="64611-247">Entry</span></span> | <span data-ttu-id="64611-248">Valor</span><span class="sxs-lookup"><span data-stu-id="64611-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="64611-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="64611-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="64611-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64611-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="64611-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="64611-251">System-Only</span></span>            | <span data-ttu-id="64611-252">Falso</span><span class="sxs-lookup"><span data-stu-id="64611-252">False</span></span>                                        |
| <span data-ttu-id="64611-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="64611-253">Is-Single-Valued</span></span>       | <span data-ttu-id="64611-254">True</span><span class="sxs-lookup"><span data-stu-id="64611-254">True</span></span>                                         |
| <span data-ttu-id="64611-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="64611-255">Is Indexed</span></span>             | <span data-ttu-id="64611-256">Falso</span><span class="sxs-lookup"><span data-stu-id="64611-256">False</span></span>                                        |
| <span data-ttu-id="64611-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="64611-257">In Global Catalog</span></span>      | <span data-ttu-id="64611-258">Falso</span><span class="sxs-lookup"><span data-stu-id="64611-258">False</span></span>                                        |
| <span data-ttu-id="64611-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="64611-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="64611-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="64611-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="64611-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64611-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="64611-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64611-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="64611-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64611-263">Search-Flags</span></span>           | <span data-ttu-id="64611-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64611-264">0x00000000</span></span>                                   |
| <span data-ttu-id="64611-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64611-265">System-Flags</span></span>           | <span data-ttu-id="64611-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64611-266">0x00000010</span></span>                                   |
| <span data-ttu-id="64611-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="64611-267">Classes used in</span></span>        | [<span data-ttu-id="64611-268">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="64611-268">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





