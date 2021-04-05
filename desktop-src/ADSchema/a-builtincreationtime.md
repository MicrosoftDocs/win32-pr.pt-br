---
title: Atributo Builtin-Creation-time
description: O atributo Builtin-Creation-time é usado para dar suporte à replicação em domínios do Windows NT 4,0.
ms.assetid: b3da9913-8c7b-481b-ae47-6b124544f1e2
ms.tgt_platform: multiple
keywords:
- Atributo de AD Builtin-Creation-time
- Esquema de AD do atributo builtinCreationTime
topic_type:
- apiref
api_name:
- Builtin-Creation-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54d5b6d37ee0242999afd47415cb067abe26e7fd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825432"
---
# <a name="builtin-creation-time-attribute"></a><span data-ttu-id="7a13a-105">Atributo Builtin-Creation-time</span><span class="sxs-lookup"><span data-stu-id="7a13a-105">Builtin-Creation-Time attribute</span></span>

<span data-ttu-id="7a13a-106">O atributo **BuiltIn-Creation-time** é usado para dar suporte à replicação em domínios do Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="7a13a-106">The **Builtin-Creation-Time** attribute is used to support replication to Windows NT 4.0 domains.</span></span>



| <span data-ttu-id="7a13a-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="7a13a-107">Entry</span></span> | <span data-ttu-id="7a13a-108">Valor</span><span class="sxs-lookup"><span data-stu-id="7a13a-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="7a13a-109">CN</span><span class="sxs-lookup"><span data-stu-id="7a13a-109">CN</span></span>                | <span data-ttu-id="7a13a-110">Interno – tempo de criação</span><span class="sxs-lookup"><span data-stu-id="7a13a-110">Builtin-Creation-Time</span></span>                |
| <span data-ttu-id="7a13a-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7a13a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7a13a-112">builtinCreationTime</span><span class="sxs-lookup"><span data-stu-id="7a13a-112">builtinCreationTime</span></span>                  |
| <span data-ttu-id="7a13a-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="7a13a-113">Size</span></span>              | <span data-ttu-id="7a13a-114">8 bytes</span><span class="sxs-lookup"><span data-stu-id="7a13a-114">8 bytes</span></span>                              |
| <span data-ttu-id="7a13a-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="7a13a-115">Update Privilege</span></span>  | <span data-ttu-id="7a13a-116">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="7a13a-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="7a13a-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="7a13a-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="7a13a-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7a13a-118">Attribute-Id</span></span>      | <span data-ttu-id="7a13a-119">1.2.840.113556.1.4.13</span><span class="sxs-lookup"><span data-stu-id="7a13a-119">1.2.840.113556.1.4.13</span></span>                |
| <span data-ttu-id="7a13a-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7a13a-120">System-Id-Guid</span></span>    | <span data-ttu-id="7a13a-121">bf96792f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="7a13a-121">bf96792f-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="7a13a-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a13a-122">Syntax</span></span>            | [<span data-ttu-id="7a13a-123">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="7a13a-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="7a13a-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="7a13a-124">Implementations</span></span>

-   [<span data-ttu-id="7a13a-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7a13a-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7a13a-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7a13a-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7a13a-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7a13a-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7a13a-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7a13a-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7a13a-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7a13a-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7a13a-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7a13a-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7a13a-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7a13a-131">Windows 2000 Server</span></span>



| <span data-ttu-id="7a13a-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="7a13a-132">Entry</span></span> | <span data-ttu-id="7a13a-133">Valor</span><span class="sxs-lookup"><span data-stu-id="7a13a-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7a13a-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="7a13a-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7a13a-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a13a-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7a13a-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a13a-136">System-Only</span></span>            | <span data-ttu-id="7a13a-137">Falso</span><span class="sxs-lookup"><span data-stu-id="7a13a-137">False</span></span>                                        |
| <span data-ttu-id="7a13a-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7a13a-138">Is-Single-Valued</span></span>       | <span data-ttu-id="7a13a-139">True</span><span class="sxs-lookup"><span data-stu-id="7a13a-139">True</span></span>                                         |
| <span data-ttu-id="7a13a-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="7a13a-140">Is Indexed</span></span>             | <span data-ttu-id="7a13a-141">Falso</span><span class="sxs-lookup"><span data-stu-id="7a13a-141">False</span></span>                                        |
| <span data-ttu-id="7a13a-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7a13a-142">In Global Catalog</span></span>      | <span data-ttu-id="7a13a-143">Falso</span><span class="sxs-lookup"><span data-stu-id="7a13a-143">False</span></span>                                        |
| <span data-ttu-id="7a13a-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7a13a-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a13a-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7a13a-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7a13a-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a13a-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="7a13a-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a13a-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="7a13a-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a13a-148">Search-Flags</span></span>           | <span data-ttu-id="7a13a-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a13a-149">0x00000000</span></span>                                   |
| <span data-ttu-id="7a13a-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a13a-150">System-Flags</span></span>           | <span data-ttu-id="7a13a-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a13a-151">0x00000010</span></span>                                   |
| <span data-ttu-id="7a13a-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7a13a-152">Classes used in</span></span>        | [<span data-ttu-id="7a13a-153">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="7a13a-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7a13a-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7a13a-154">Windows Server 2003</span></span>



| <span data-ttu-id="7a13a-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="7a13a-155">Entry</span></span> | <span data-ttu-id="7a13a-156">Valor</span><span class="sxs-lookup"><span data-stu-id="7a13a-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7a13a-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="7a13a-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7a13a-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a13a-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7a13a-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a13a-159">System-Only</span></span>            | <span data-ttu-id="7a13a-160">Falso</span><span class="sxs-lookup"><span data-stu-id="7a13a-160">False</span></span>                                        |
| <span data-ttu-id="7a13a-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7a13a-161">Is-Single-Valued</span></span>       | <span data-ttu-id="7a13a-162">True</span><span class="sxs-lookup"><span data-stu-id="7a13a-162">True</span></span>                                         |
| <span data-ttu-id="7a13a-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="7a13a-163">Is Indexed</span></span>             | <span data-ttu-id="7a13a-164">Falso</span><span class="sxs-lookup"><span data-stu-id="7a13a-164">False</span></span>                                        |
| <span data-ttu-id="7a13a-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7a13a-165">In Global Catalog</span></span>      | <span data-ttu-id="7a13a-166">Falso</span><span class="sxs-lookup"><span data-stu-id="7a13a-166">False</span></span>                                        |
| <span data-ttu-id="7a13a-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7a13a-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a13a-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7a13a-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7a13a-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a13a-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="7a13a-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a13a-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="7a13a-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a13a-171">Search-Flags</span></span>           | <span data-ttu-id="7a13a-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a13a-172">0x00000000</span></span>                                   |
| <span data-ttu-id="7a13a-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a13a-173">System-Flags</span></span>           | <span data-ttu-id="7a13a-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a13a-174">0x00000010</span></span>                                   |
| <span data-ttu-id="7a13a-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7a13a-175">Classes used in</span></span>        | [<span data-ttu-id="7a13a-176">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="7a13a-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7a13a-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7a13a-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7a13a-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="7a13a-178">Entry</span></span> | <span data-ttu-id="7a13a-179">Valor</span><span class="sxs-lookup"><span data-stu-id="7a13a-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7a13a-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="7a13a-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7a13a-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a13a-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7a13a-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a13a-182">System-Only</span></span>            | <span data-ttu-id="7a13a-183">Falso</span><span class="sxs-lookup"><span data-stu-id="7a13a-183">False</span></span>                                        |
| <span data-ttu-id="7a13a-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7a13a-184">Is-Single-Valued</span></span>       | <span data-ttu-id="7a13a-185">True</span><span class="sxs-lookup"><span data-stu-id="7a13a-185">True</span></span>                                         |
| <span data-ttu-id="7a13a-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="7a13a-186">Is Indexed</span></span>             | <span data-ttu-id="7a13a-187">Falso</span><span class="sxs-lookup"><span data-stu-id="7a13a-187">False</span></span>                                        |
| <span data-ttu-id="7a13a-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7a13a-188">In Global Catalog</span></span>      | <span data-ttu-id="7a13a-189">Falso</span><span class="sxs-lookup"><span data-stu-id="7a13a-189">False</span></span>                                        |
| <span data-ttu-id="7a13a-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7a13a-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a13a-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7a13a-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7a13a-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a13a-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="7a13a-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a13a-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="7a13a-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a13a-194">Search-Flags</span></span>           | <span data-ttu-id="7a13a-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a13a-195">0x00000000</span></span>                                   |
| <span data-ttu-id="7a13a-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a13a-196">System-Flags</span></span>           | <span data-ttu-id="7a13a-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a13a-197">0x00000010</span></span>                                   |
| <span data-ttu-id="7a13a-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7a13a-198">Classes used in</span></span>        | [<span data-ttu-id="7a13a-199">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="7a13a-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7a13a-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a13a-200">Windows Server 2008</span></span>



| <span data-ttu-id="7a13a-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="7a13a-201">Entry</span></span> | <span data-ttu-id="7a13a-202">Valor</span><span class="sxs-lookup"><span data-stu-id="7a13a-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7a13a-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="7a13a-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7a13a-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a13a-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7a13a-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a13a-205">System-Only</span></span>            | <span data-ttu-id="7a13a-206">Falso</span><span class="sxs-lookup"><span data-stu-id="7a13a-206">False</span></span>                                        |
| <span data-ttu-id="7a13a-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7a13a-207">Is-Single-Valued</span></span>       | <span data-ttu-id="7a13a-208">True</span><span class="sxs-lookup"><span data-stu-id="7a13a-208">True</span></span>                                         |
| <span data-ttu-id="7a13a-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="7a13a-209">Is Indexed</span></span>             | <span data-ttu-id="7a13a-210">Falso</span><span class="sxs-lookup"><span data-stu-id="7a13a-210">False</span></span>                                        |
| <span data-ttu-id="7a13a-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7a13a-211">In Global Catalog</span></span>      | <span data-ttu-id="7a13a-212">Falso</span><span class="sxs-lookup"><span data-stu-id="7a13a-212">False</span></span>                                        |
| <span data-ttu-id="7a13a-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7a13a-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a13a-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7a13a-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7a13a-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a13a-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="7a13a-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a13a-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="7a13a-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a13a-217">Search-Flags</span></span>           | <span data-ttu-id="7a13a-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a13a-218">0x00000000</span></span>                                   |
| <span data-ttu-id="7a13a-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a13a-219">System-Flags</span></span>           | <span data-ttu-id="7a13a-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a13a-220">0x00000010</span></span>                                   |
| <span data-ttu-id="7a13a-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7a13a-221">Classes used in</span></span>        | [<span data-ttu-id="7a13a-222">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="7a13a-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7a13a-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7a13a-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7a13a-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="7a13a-224">Entry</span></span> | <span data-ttu-id="7a13a-225">Valor</span><span class="sxs-lookup"><span data-stu-id="7a13a-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7a13a-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="7a13a-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7a13a-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a13a-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7a13a-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a13a-228">System-Only</span></span>            | <span data-ttu-id="7a13a-229">Falso</span><span class="sxs-lookup"><span data-stu-id="7a13a-229">False</span></span>                                        |
| <span data-ttu-id="7a13a-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7a13a-230">Is-Single-Valued</span></span>       | <span data-ttu-id="7a13a-231">True</span><span class="sxs-lookup"><span data-stu-id="7a13a-231">True</span></span>                                         |
| <span data-ttu-id="7a13a-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="7a13a-232">Is Indexed</span></span>             | <span data-ttu-id="7a13a-233">Falso</span><span class="sxs-lookup"><span data-stu-id="7a13a-233">False</span></span>                                        |
| <span data-ttu-id="7a13a-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7a13a-234">In Global Catalog</span></span>      | <span data-ttu-id="7a13a-235">Falso</span><span class="sxs-lookup"><span data-stu-id="7a13a-235">False</span></span>                                        |
| <span data-ttu-id="7a13a-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7a13a-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a13a-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7a13a-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7a13a-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a13a-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="7a13a-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a13a-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="7a13a-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a13a-240">Search-Flags</span></span>           | <span data-ttu-id="7a13a-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a13a-241">0x00000000</span></span>                                   |
| <span data-ttu-id="7a13a-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a13a-242">System-Flags</span></span>           | <span data-ttu-id="7a13a-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a13a-243">0x00000010</span></span>                                   |
| <span data-ttu-id="7a13a-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7a13a-244">Classes used in</span></span>        | [<span data-ttu-id="7a13a-245">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="7a13a-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7a13a-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7a13a-246">Windows Server 2012</span></span>



| <span data-ttu-id="7a13a-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="7a13a-247">Entry</span></span> | <span data-ttu-id="7a13a-248">Valor</span><span class="sxs-lookup"><span data-stu-id="7a13a-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="7a13a-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="7a13a-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="7a13a-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a13a-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="7a13a-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a13a-251">System-Only</span></span>            | <span data-ttu-id="7a13a-252">Falso</span><span class="sxs-lookup"><span data-stu-id="7a13a-252">False</span></span>                                        |
| <span data-ttu-id="7a13a-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7a13a-253">Is-Single-Valued</span></span>       | <span data-ttu-id="7a13a-254">True</span><span class="sxs-lookup"><span data-stu-id="7a13a-254">True</span></span>                                         |
| <span data-ttu-id="7a13a-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="7a13a-255">Is Indexed</span></span>             | <span data-ttu-id="7a13a-256">Falso</span><span class="sxs-lookup"><span data-stu-id="7a13a-256">False</span></span>                                        |
| <span data-ttu-id="7a13a-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7a13a-257">In Global Catalog</span></span>      | <span data-ttu-id="7a13a-258">Falso</span><span class="sxs-lookup"><span data-stu-id="7a13a-258">False</span></span>                                        |
| <span data-ttu-id="7a13a-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7a13a-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a13a-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7a13a-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="7a13a-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a13a-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="7a13a-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a13a-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="7a13a-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a13a-263">Search-Flags</span></span>           | <span data-ttu-id="7a13a-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a13a-264">0x00000000</span></span>                                   |
| <span data-ttu-id="7a13a-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a13a-265">System-Flags</span></span>           | <span data-ttu-id="7a13a-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a13a-266">0x00000010</span></span>                                   |
| <span data-ttu-id="7a13a-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7a13a-267">Classes used in</span></span>        | [<span data-ttu-id="7a13a-268">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="7a13a-268">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





