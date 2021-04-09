---
title: Atributo Builtin-Modified-Count
description: O atributo Builtin-Modified-Count é usado para dar suporte à replicação em domínios do Windows NT 4,0.
ms.assetid: e5a0f299-1e69-4b47-a0b1-e5bcf7bd47eb
ms.tgt_platform: multiple
keywords:
- Atributo de AD de atributos de contagem Builtin-Modified
- Esquema de AD do atributo builtinModifiedCount
topic_type:
- apiref
api_name:
- Builtin-Modified-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7731cd27ef5cb5d25dcd4bced4dbc5932225ba5d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104087131"
---
# <a name="builtin-modified-count-attribute"></a><span data-ttu-id="1143f-105">Atributo Builtin-Modified-Count</span><span class="sxs-lookup"><span data-stu-id="1143f-105">Builtin-Modified-Count attribute</span></span>

<span data-ttu-id="1143f-106">O atributo **BuiltIn-Modified-Count** é usado para dar suporte à replicação em domínios do Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="1143f-106">The **Builtin-Modified-Count** attribute is used to support replication to Windows NT 4.0 domains.</span></span>



| <span data-ttu-id="1143f-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="1143f-107">Entry</span></span> | <span data-ttu-id="1143f-108">Valor</span><span class="sxs-lookup"><span data-stu-id="1143f-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="1143f-109">CN</span><span class="sxs-lookup"><span data-stu-id="1143f-109">CN</span></span>                | <span data-ttu-id="1143f-110">Builtin-modificado-contagem</span><span class="sxs-lookup"><span data-stu-id="1143f-110">Builtin-Modified-Count</span></span>               |
| <span data-ttu-id="1143f-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="1143f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1143f-112">builtinModifiedCount</span><span class="sxs-lookup"><span data-stu-id="1143f-112">builtinModifiedCount</span></span>                 |
| <span data-ttu-id="1143f-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="1143f-113">Size</span></span>              | <span data-ttu-id="1143f-114">8 bytes</span><span class="sxs-lookup"><span data-stu-id="1143f-114">8 bytes</span></span>                              |
| <span data-ttu-id="1143f-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="1143f-115">Update Privilege</span></span>  | <span data-ttu-id="1143f-116">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="1143f-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="1143f-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="1143f-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="1143f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1143f-118">Attribute-Id</span></span>      | <span data-ttu-id="1143f-119">1.2.840.113556.1.4.14</span><span class="sxs-lookup"><span data-stu-id="1143f-119">1.2.840.113556.1.4.14</span></span>                |
| <span data-ttu-id="1143f-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1143f-120">System-Id-Guid</span></span>    | <span data-ttu-id="1143f-121">bf967930-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="1143f-121">bf967930-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="1143f-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="1143f-122">Syntax</span></span>            | [<span data-ttu-id="1143f-123">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="1143f-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="1143f-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="1143f-124">Implementations</span></span>

-   [<span data-ttu-id="1143f-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1143f-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1143f-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1143f-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1143f-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1143f-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1143f-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1143f-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1143f-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1143f-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1143f-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1143f-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1143f-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1143f-131">Windows 2000 Server</span></span>



| <span data-ttu-id="1143f-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="1143f-132">Entry</span></span> | <span data-ttu-id="1143f-133">Valor</span><span class="sxs-lookup"><span data-stu-id="1143f-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="1143f-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="1143f-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="1143f-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1143f-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="1143f-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="1143f-136">System-Only</span></span>            | <span data-ttu-id="1143f-137">Falso</span><span class="sxs-lookup"><span data-stu-id="1143f-137">False</span></span>                                        |
| <span data-ttu-id="1143f-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1143f-138">Is-Single-Valued</span></span>       | <span data-ttu-id="1143f-139">True</span><span class="sxs-lookup"><span data-stu-id="1143f-139">True</span></span>                                         |
| <span data-ttu-id="1143f-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="1143f-140">Is Indexed</span></span>             | <span data-ttu-id="1143f-141">Falso</span><span class="sxs-lookup"><span data-stu-id="1143f-141">False</span></span>                                        |
| <span data-ttu-id="1143f-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1143f-142">In Global Catalog</span></span>      | <span data-ttu-id="1143f-143">Falso</span><span class="sxs-lookup"><span data-stu-id="1143f-143">False</span></span>                                        |
| <span data-ttu-id="1143f-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1143f-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="1143f-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1143f-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="1143f-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1143f-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="1143f-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1143f-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="1143f-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1143f-148">Search-Flags</span></span>           | <span data-ttu-id="1143f-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1143f-149">0x00000000</span></span>                                   |
| <span data-ttu-id="1143f-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1143f-150">System-Flags</span></span>           | <span data-ttu-id="1143f-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1143f-151">0x00000010</span></span>                                   |
| <span data-ttu-id="1143f-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1143f-152">Classes used in</span></span>        | [<span data-ttu-id="1143f-153">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="1143f-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1143f-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1143f-154">Windows Server 2003</span></span>



| <span data-ttu-id="1143f-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="1143f-155">Entry</span></span> | <span data-ttu-id="1143f-156">Valor</span><span class="sxs-lookup"><span data-stu-id="1143f-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="1143f-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="1143f-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="1143f-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1143f-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="1143f-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="1143f-159">System-Only</span></span>            | <span data-ttu-id="1143f-160">Falso</span><span class="sxs-lookup"><span data-stu-id="1143f-160">False</span></span>                                        |
| <span data-ttu-id="1143f-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1143f-161">Is-Single-Valued</span></span>       | <span data-ttu-id="1143f-162">True</span><span class="sxs-lookup"><span data-stu-id="1143f-162">True</span></span>                                         |
| <span data-ttu-id="1143f-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="1143f-163">Is Indexed</span></span>             | <span data-ttu-id="1143f-164">Falso</span><span class="sxs-lookup"><span data-stu-id="1143f-164">False</span></span>                                        |
| <span data-ttu-id="1143f-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1143f-165">In Global Catalog</span></span>      | <span data-ttu-id="1143f-166">Falso</span><span class="sxs-lookup"><span data-stu-id="1143f-166">False</span></span>                                        |
| <span data-ttu-id="1143f-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1143f-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="1143f-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1143f-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="1143f-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1143f-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="1143f-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1143f-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="1143f-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1143f-171">Search-Flags</span></span>           | <span data-ttu-id="1143f-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1143f-172">0x00000000</span></span>                                   |
| <span data-ttu-id="1143f-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1143f-173">System-Flags</span></span>           | <span data-ttu-id="1143f-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1143f-174">0x00000010</span></span>                                   |
| <span data-ttu-id="1143f-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1143f-175">Classes used in</span></span>        | [<span data-ttu-id="1143f-176">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="1143f-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1143f-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1143f-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1143f-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="1143f-178">Entry</span></span> | <span data-ttu-id="1143f-179">Valor</span><span class="sxs-lookup"><span data-stu-id="1143f-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="1143f-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="1143f-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="1143f-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1143f-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="1143f-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="1143f-182">System-Only</span></span>            | <span data-ttu-id="1143f-183">Falso</span><span class="sxs-lookup"><span data-stu-id="1143f-183">False</span></span>                                        |
| <span data-ttu-id="1143f-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1143f-184">Is-Single-Valued</span></span>       | <span data-ttu-id="1143f-185">True</span><span class="sxs-lookup"><span data-stu-id="1143f-185">True</span></span>                                         |
| <span data-ttu-id="1143f-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="1143f-186">Is Indexed</span></span>             | <span data-ttu-id="1143f-187">Falso</span><span class="sxs-lookup"><span data-stu-id="1143f-187">False</span></span>                                        |
| <span data-ttu-id="1143f-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1143f-188">In Global Catalog</span></span>      | <span data-ttu-id="1143f-189">Falso</span><span class="sxs-lookup"><span data-stu-id="1143f-189">False</span></span>                                        |
| <span data-ttu-id="1143f-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1143f-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="1143f-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1143f-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="1143f-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1143f-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="1143f-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1143f-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="1143f-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1143f-194">Search-Flags</span></span>           | <span data-ttu-id="1143f-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1143f-195">0x00000000</span></span>                                   |
| <span data-ttu-id="1143f-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1143f-196">System-Flags</span></span>           | <span data-ttu-id="1143f-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1143f-197">0x00000010</span></span>                                   |
| <span data-ttu-id="1143f-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1143f-198">Classes used in</span></span>        | [<span data-ttu-id="1143f-199">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="1143f-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1143f-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1143f-200">Windows Server 2008</span></span>



| <span data-ttu-id="1143f-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="1143f-201">Entry</span></span> | <span data-ttu-id="1143f-202">Valor</span><span class="sxs-lookup"><span data-stu-id="1143f-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="1143f-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="1143f-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="1143f-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1143f-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="1143f-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="1143f-205">System-Only</span></span>            | <span data-ttu-id="1143f-206">Falso</span><span class="sxs-lookup"><span data-stu-id="1143f-206">False</span></span>                                        |
| <span data-ttu-id="1143f-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1143f-207">Is-Single-Valued</span></span>       | <span data-ttu-id="1143f-208">True</span><span class="sxs-lookup"><span data-stu-id="1143f-208">True</span></span>                                         |
| <span data-ttu-id="1143f-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="1143f-209">Is Indexed</span></span>             | <span data-ttu-id="1143f-210">Falso</span><span class="sxs-lookup"><span data-stu-id="1143f-210">False</span></span>                                        |
| <span data-ttu-id="1143f-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1143f-211">In Global Catalog</span></span>      | <span data-ttu-id="1143f-212">Falso</span><span class="sxs-lookup"><span data-stu-id="1143f-212">False</span></span>                                        |
| <span data-ttu-id="1143f-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1143f-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="1143f-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1143f-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="1143f-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1143f-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="1143f-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1143f-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="1143f-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1143f-217">Search-Flags</span></span>           | <span data-ttu-id="1143f-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1143f-218">0x00000000</span></span>                                   |
| <span data-ttu-id="1143f-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1143f-219">System-Flags</span></span>           | <span data-ttu-id="1143f-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1143f-220">0x00000010</span></span>                                   |
| <span data-ttu-id="1143f-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1143f-221">Classes used in</span></span>        | [<span data-ttu-id="1143f-222">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="1143f-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1143f-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1143f-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1143f-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="1143f-224">Entry</span></span> | <span data-ttu-id="1143f-225">Valor</span><span class="sxs-lookup"><span data-stu-id="1143f-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="1143f-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="1143f-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="1143f-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1143f-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="1143f-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="1143f-228">System-Only</span></span>            | <span data-ttu-id="1143f-229">Falso</span><span class="sxs-lookup"><span data-stu-id="1143f-229">False</span></span>                                        |
| <span data-ttu-id="1143f-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1143f-230">Is-Single-Valued</span></span>       | <span data-ttu-id="1143f-231">True</span><span class="sxs-lookup"><span data-stu-id="1143f-231">True</span></span>                                         |
| <span data-ttu-id="1143f-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="1143f-232">Is Indexed</span></span>             | <span data-ttu-id="1143f-233">Falso</span><span class="sxs-lookup"><span data-stu-id="1143f-233">False</span></span>                                        |
| <span data-ttu-id="1143f-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1143f-234">In Global Catalog</span></span>      | <span data-ttu-id="1143f-235">Falso</span><span class="sxs-lookup"><span data-stu-id="1143f-235">False</span></span>                                        |
| <span data-ttu-id="1143f-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1143f-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="1143f-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1143f-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="1143f-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1143f-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="1143f-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1143f-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="1143f-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1143f-240">Search-Flags</span></span>           | <span data-ttu-id="1143f-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1143f-241">0x00000000</span></span>                                   |
| <span data-ttu-id="1143f-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1143f-242">System-Flags</span></span>           | <span data-ttu-id="1143f-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1143f-243">0x00000010</span></span>                                   |
| <span data-ttu-id="1143f-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1143f-244">Classes used in</span></span>        | [<span data-ttu-id="1143f-245">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="1143f-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1143f-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1143f-246">Windows Server 2012</span></span>



| <span data-ttu-id="1143f-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="1143f-247">Entry</span></span> | <span data-ttu-id="1143f-248">Valor</span><span class="sxs-lookup"><span data-stu-id="1143f-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="1143f-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="1143f-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="1143f-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1143f-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="1143f-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="1143f-251">System-Only</span></span>            | <span data-ttu-id="1143f-252">Falso</span><span class="sxs-lookup"><span data-stu-id="1143f-252">False</span></span>                                        |
| <span data-ttu-id="1143f-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1143f-253">Is-Single-Valued</span></span>       | <span data-ttu-id="1143f-254">True</span><span class="sxs-lookup"><span data-stu-id="1143f-254">True</span></span>                                         |
| <span data-ttu-id="1143f-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="1143f-255">Is Indexed</span></span>             | <span data-ttu-id="1143f-256">Falso</span><span class="sxs-lookup"><span data-stu-id="1143f-256">False</span></span>                                        |
| <span data-ttu-id="1143f-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1143f-257">In Global Catalog</span></span>      | <span data-ttu-id="1143f-258">Falso</span><span class="sxs-lookup"><span data-stu-id="1143f-258">False</span></span>                                        |
| <span data-ttu-id="1143f-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1143f-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="1143f-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1143f-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="1143f-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1143f-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="1143f-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1143f-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="1143f-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1143f-263">Search-Flags</span></span>           | <span data-ttu-id="1143f-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1143f-264">0x00000000</span></span>                                   |
| <span data-ttu-id="1143f-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1143f-265">System-Flags</span></span>           | <span data-ttu-id="1143f-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1143f-266">0x00000010</span></span>                                   |
| <span data-ttu-id="1143f-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1143f-267">Classes used in</span></span>        | [<span data-ttu-id="1143f-268">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="1143f-268">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





