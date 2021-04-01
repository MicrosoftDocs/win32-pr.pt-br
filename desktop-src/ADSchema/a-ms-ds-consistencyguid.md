---
title: Atributo MS-DS-Consistency-GUID
description: Esse atributo é usado para verificar a consistência entre o diretório e outro objeto, banco de dados ou aplicativo, comparando GUIDs.
ms.assetid: 1372f46a-5569-4b06-9803-7d3862cdb745
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo MS-DS-Consistency-GUID
- Esquema de AD do atributo mS-DS-ConsistencyGuid
topic_type:
- apiref
api_name:
- MS-DS-Consistency-Guid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fdbea1e9fba4ac28f968fdd61a054f55fe47deb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825227"
---
# <a name="ms-ds-consistency-guid-attribute"></a><span data-ttu-id="b13bb-105">Atributo MS-DS-Consistency-GUID</span><span class="sxs-lookup"><span data-stu-id="b13bb-105">MS-DS-Consistency-Guid attribute</span></span>

<span data-ttu-id="b13bb-106">Esse atributo é usado para verificar a consistência entre o diretório e outro objeto, banco de dados ou aplicativo, comparando GUIDs.</span><span class="sxs-lookup"><span data-stu-id="b13bb-106">This attribute is used to check consistency between the directory and another object, database, or application, by comparing GUIDs.</span></span>



| <span data-ttu-id="b13bb-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="b13bb-107">Entry</span></span> | <span data-ttu-id="b13bb-108">Valor</span><span class="sxs-lookup"><span data-stu-id="b13bb-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="b13bb-109">CN</span><span class="sxs-lookup"><span data-stu-id="b13bb-109">CN</span></span>                | <span data-ttu-id="b13bb-110">MS-DS-Consistency-Guid</span><span class="sxs-lookup"><span data-stu-id="b13bb-110">MS-DS-Consistency-Guid</span></span>                                |
| <span data-ttu-id="b13bb-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="b13bb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b13bb-112">mS-DS-ConsistencyGuid</span><span class="sxs-lookup"><span data-stu-id="b13bb-112">mS-DS-ConsistencyGuid</span></span>                                 |
| <span data-ttu-id="b13bb-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="b13bb-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="b13bb-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="b13bb-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="b13bb-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="b13bb-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="b13bb-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b13bb-116">Attribute-Id</span></span>      | <span data-ttu-id="b13bb-117">1.2.840.113556.1.4.1360</span><span class="sxs-lookup"><span data-stu-id="b13bb-117">1.2.840.113556.1.4.1360</span></span>                               |
| <span data-ttu-id="b13bb-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="b13bb-118">System-Id-Guid</span></span>    | <span data-ttu-id="b13bb-119">23773dc2-b63a-11d2-90e1-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="b13bb-119">23773dc2-b63a-11d2-90e1-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="b13bb-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="b13bb-120">Syntax</span></span>            | [<span data-ttu-id="b13bb-121">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="b13bb-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="b13bb-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="b13bb-122">Implementations</span></span>

-   [<span data-ttu-id="b13bb-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b13bb-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b13bb-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b13bb-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b13bb-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="b13bb-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b13bb-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b13bb-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b13bb-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b13bb-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b13bb-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b13bb-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b13bb-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b13bb-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b13bb-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b13bb-130">Windows 2000 Server</span></span>



| <span data-ttu-id="b13bb-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="b13bb-131">Entry</span></span> | <span data-ttu-id="b13bb-132">Valor</span><span class="sxs-lookup"><span data-stu-id="b13bb-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b13bb-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="b13bb-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b13bb-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b13bb-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b13bb-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="b13bb-135">System-Only</span></span>            | <span data-ttu-id="b13bb-136">Falso</span><span class="sxs-lookup"><span data-stu-id="b13bb-136">False</span></span>                           |
| <span data-ttu-id="b13bb-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b13bb-137">Is-Single-Valued</span></span>       | <span data-ttu-id="b13bb-138">True</span><span class="sxs-lookup"><span data-stu-id="b13bb-138">True</span></span>                            |
| <span data-ttu-id="b13bb-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="b13bb-139">Is Indexed</span></span>             | <span data-ttu-id="b13bb-140">Falso</span><span class="sxs-lookup"><span data-stu-id="b13bb-140">False</span></span>                           |
| <span data-ttu-id="b13bb-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b13bb-141">In Global Catalog</span></span>      | <span data-ttu-id="b13bb-142">Falso</span><span class="sxs-lookup"><span data-stu-id="b13bb-142">False</span></span>                           |
| <span data-ttu-id="b13bb-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b13bb-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="b13bb-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b13bb-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b13bb-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b13bb-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b13bb-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b13bb-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b13bb-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b13bb-147">Search-Flags</span></span>           | <span data-ttu-id="b13bb-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b13bb-148">0x00000000</span></span>                      |
| <span data-ttu-id="b13bb-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b13bb-149">System-Flags</span></span>           | <span data-ttu-id="b13bb-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b13bb-150">0x00000010</span></span>                      |
| <span data-ttu-id="b13bb-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b13bb-151">Classes used in</span></span>        | [<span data-ttu-id="b13bb-152">**Início**</span><span class="sxs-lookup"><span data-stu-id="b13bb-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b13bb-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b13bb-153">Windows Server 2003</span></span>



| <span data-ttu-id="b13bb-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="b13bb-154">Entry</span></span> | <span data-ttu-id="b13bb-155">Valor</span><span class="sxs-lookup"><span data-stu-id="b13bb-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b13bb-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="b13bb-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b13bb-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b13bb-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b13bb-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="b13bb-158">System-Only</span></span>            | <span data-ttu-id="b13bb-159">Falso</span><span class="sxs-lookup"><span data-stu-id="b13bb-159">False</span></span>                           |
| <span data-ttu-id="b13bb-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b13bb-160">Is-Single-Valued</span></span>       | <span data-ttu-id="b13bb-161">True</span><span class="sxs-lookup"><span data-stu-id="b13bb-161">True</span></span>                            |
| <span data-ttu-id="b13bb-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="b13bb-162">Is Indexed</span></span>             | <span data-ttu-id="b13bb-163">Falso</span><span class="sxs-lookup"><span data-stu-id="b13bb-163">False</span></span>                           |
| <span data-ttu-id="b13bb-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b13bb-164">In Global Catalog</span></span>      | <span data-ttu-id="b13bb-165">Falso</span><span class="sxs-lookup"><span data-stu-id="b13bb-165">False</span></span>                           |
| <span data-ttu-id="b13bb-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b13bb-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="b13bb-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b13bb-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b13bb-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b13bb-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b13bb-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b13bb-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b13bb-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b13bb-170">Search-Flags</span></span>           | <span data-ttu-id="b13bb-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b13bb-171">0x00000000</span></span>                      |
| <span data-ttu-id="b13bb-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b13bb-172">System-Flags</span></span>           | <span data-ttu-id="b13bb-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b13bb-173">0x00000010</span></span>                      |
| <span data-ttu-id="b13bb-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b13bb-174">Classes used in</span></span>        | [<span data-ttu-id="b13bb-175">**Início**</span><span class="sxs-lookup"><span data-stu-id="b13bb-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b13bb-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="b13bb-176">ADAM</span></span>



| <span data-ttu-id="b13bb-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="b13bb-177">Entry</span></span> | <span data-ttu-id="b13bb-178">Valor</span><span class="sxs-lookup"><span data-stu-id="b13bb-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b13bb-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="b13bb-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b13bb-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b13bb-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b13bb-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="b13bb-181">System-Only</span></span>            | <span data-ttu-id="b13bb-182">Falso</span><span class="sxs-lookup"><span data-stu-id="b13bb-182">False</span></span>                           |
| <span data-ttu-id="b13bb-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b13bb-183">Is-Single-Valued</span></span>       | <span data-ttu-id="b13bb-184">True</span><span class="sxs-lookup"><span data-stu-id="b13bb-184">True</span></span>                            |
| <span data-ttu-id="b13bb-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="b13bb-185">Is Indexed</span></span>             | <span data-ttu-id="b13bb-186">Falso</span><span class="sxs-lookup"><span data-stu-id="b13bb-186">False</span></span>                           |
| <span data-ttu-id="b13bb-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b13bb-187">In Global Catalog</span></span>      | <span data-ttu-id="b13bb-188">Falso</span><span class="sxs-lookup"><span data-stu-id="b13bb-188">False</span></span>                           |
| <span data-ttu-id="b13bb-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b13bb-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="b13bb-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b13bb-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b13bb-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b13bb-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b13bb-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b13bb-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b13bb-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b13bb-193">Search-Flags</span></span>           | <span data-ttu-id="b13bb-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b13bb-194">0x00000000</span></span>                      |
| <span data-ttu-id="b13bb-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b13bb-195">System-Flags</span></span>           | <span data-ttu-id="b13bb-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b13bb-196">0x00000010</span></span>                      |
| <span data-ttu-id="b13bb-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b13bb-197">Classes used in</span></span>        | [<span data-ttu-id="b13bb-198">**Início**</span><span class="sxs-lookup"><span data-stu-id="b13bb-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b13bb-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b13bb-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b13bb-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="b13bb-200">Entry</span></span> | <span data-ttu-id="b13bb-201">Valor</span><span class="sxs-lookup"><span data-stu-id="b13bb-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b13bb-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="b13bb-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b13bb-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b13bb-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b13bb-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="b13bb-204">System-Only</span></span>            | <span data-ttu-id="b13bb-205">Falso</span><span class="sxs-lookup"><span data-stu-id="b13bb-205">False</span></span>                           |
| <span data-ttu-id="b13bb-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b13bb-206">Is-Single-Valued</span></span>       | <span data-ttu-id="b13bb-207">True</span><span class="sxs-lookup"><span data-stu-id="b13bb-207">True</span></span>                            |
| <span data-ttu-id="b13bb-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="b13bb-208">Is Indexed</span></span>             | <span data-ttu-id="b13bb-209">Falso</span><span class="sxs-lookup"><span data-stu-id="b13bb-209">False</span></span>                           |
| <span data-ttu-id="b13bb-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b13bb-210">In Global Catalog</span></span>      | <span data-ttu-id="b13bb-211">Falso</span><span class="sxs-lookup"><span data-stu-id="b13bb-211">False</span></span>                           |
| <span data-ttu-id="b13bb-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b13bb-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="b13bb-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b13bb-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b13bb-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b13bb-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b13bb-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b13bb-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b13bb-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b13bb-216">Search-Flags</span></span>           | <span data-ttu-id="b13bb-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b13bb-217">0x00000000</span></span>                      |
| <span data-ttu-id="b13bb-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b13bb-218">System-Flags</span></span>           | <span data-ttu-id="b13bb-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b13bb-219">0x00000010</span></span>                      |
| <span data-ttu-id="b13bb-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b13bb-220">Classes used in</span></span>        | [<span data-ttu-id="b13bb-221">**Início**</span><span class="sxs-lookup"><span data-stu-id="b13bb-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b13bb-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b13bb-222">Windows Server 2008</span></span>



| <span data-ttu-id="b13bb-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="b13bb-223">Entry</span></span> | <span data-ttu-id="b13bb-224">Valor</span><span class="sxs-lookup"><span data-stu-id="b13bb-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b13bb-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="b13bb-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b13bb-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b13bb-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b13bb-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="b13bb-227">System-Only</span></span>            | <span data-ttu-id="b13bb-228">Falso</span><span class="sxs-lookup"><span data-stu-id="b13bb-228">False</span></span>                           |
| <span data-ttu-id="b13bb-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b13bb-229">Is-Single-Valued</span></span>       | <span data-ttu-id="b13bb-230">True</span><span class="sxs-lookup"><span data-stu-id="b13bb-230">True</span></span>                            |
| <span data-ttu-id="b13bb-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="b13bb-231">Is Indexed</span></span>             | <span data-ttu-id="b13bb-232">Falso</span><span class="sxs-lookup"><span data-stu-id="b13bb-232">False</span></span>                           |
| <span data-ttu-id="b13bb-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b13bb-233">In Global Catalog</span></span>      | <span data-ttu-id="b13bb-234">Falso</span><span class="sxs-lookup"><span data-stu-id="b13bb-234">False</span></span>                           |
| <span data-ttu-id="b13bb-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b13bb-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="b13bb-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b13bb-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b13bb-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b13bb-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b13bb-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b13bb-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b13bb-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b13bb-239">Search-Flags</span></span>           | <span data-ttu-id="b13bb-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b13bb-240">0x00000000</span></span>                      |
| <span data-ttu-id="b13bb-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b13bb-241">System-Flags</span></span>           | <span data-ttu-id="b13bb-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b13bb-242">0x00000010</span></span>                      |
| <span data-ttu-id="b13bb-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b13bb-243">Classes used in</span></span>        | [<span data-ttu-id="b13bb-244">**Início**</span><span class="sxs-lookup"><span data-stu-id="b13bb-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b13bb-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b13bb-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b13bb-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="b13bb-246">Entry</span></span> | <span data-ttu-id="b13bb-247">Valor</span><span class="sxs-lookup"><span data-stu-id="b13bb-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b13bb-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="b13bb-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b13bb-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b13bb-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b13bb-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="b13bb-250">System-Only</span></span>            | <span data-ttu-id="b13bb-251">Falso</span><span class="sxs-lookup"><span data-stu-id="b13bb-251">False</span></span>                           |
| <span data-ttu-id="b13bb-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b13bb-252">Is-Single-Valued</span></span>       | <span data-ttu-id="b13bb-253">True</span><span class="sxs-lookup"><span data-stu-id="b13bb-253">True</span></span>                            |
| <span data-ttu-id="b13bb-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="b13bb-254">Is Indexed</span></span>             | <span data-ttu-id="b13bb-255">Falso</span><span class="sxs-lookup"><span data-stu-id="b13bb-255">False</span></span>                           |
| <span data-ttu-id="b13bb-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b13bb-256">In Global Catalog</span></span>      | <span data-ttu-id="b13bb-257">Falso</span><span class="sxs-lookup"><span data-stu-id="b13bb-257">False</span></span>                           |
| <span data-ttu-id="b13bb-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b13bb-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="b13bb-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b13bb-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b13bb-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b13bb-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b13bb-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b13bb-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b13bb-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b13bb-262">Search-Flags</span></span>           | <span data-ttu-id="b13bb-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b13bb-263">0x00000000</span></span>                      |
| <span data-ttu-id="b13bb-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b13bb-264">System-Flags</span></span>           | <span data-ttu-id="b13bb-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b13bb-265">0x00000010</span></span>                      |
| <span data-ttu-id="b13bb-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b13bb-266">Classes used in</span></span>        | [<span data-ttu-id="b13bb-267">**Início**</span><span class="sxs-lookup"><span data-stu-id="b13bb-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b13bb-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b13bb-268">Windows Server 2012</span></span>



| <span data-ttu-id="b13bb-269">Entrada</span><span class="sxs-lookup"><span data-stu-id="b13bb-269">Entry</span></span> | <span data-ttu-id="b13bb-270">Valor</span><span class="sxs-lookup"><span data-stu-id="b13bb-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b13bb-271">ID do link</span><span class="sxs-lookup"><span data-stu-id="b13bb-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b13bb-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b13bb-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b13bb-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="b13bb-273">System-Only</span></span>            | <span data-ttu-id="b13bb-274">Falso</span><span class="sxs-lookup"><span data-stu-id="b13bb-274">False</span></span>                           |
| <span data-ttu-id="b13bb-275">É de valor único</span><span class="sxs-lookup"><span data-stu-id="b13bb-275">Is-Single-Valued</span></span>       | <span data-ttu-id="b13bb-276">True</span><span class="sxs-lookup"><span data-stu-id="b13bb-276">True</span></span>                            |
| <span data-ttu-id="b13bb-277">É indexado</span><span class="sxs-lookup"><span data-stu-id="b13bb-277">Is Indexed</span></span>             | <span data-ttu-id="b13bb-278">Falso</span><span class="sxs-lookup"><span data-stu-id="b13bb-278">False</span></span>                           |
| <span data-ttu-id="b13bb-279">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="b13bb-279">In Global Catalog</span></span>      | <span data-ttu-id="b13bb-280">Falso</span><span class="sxs-lookup"><span data-stu-id="b13bb-280">False</span></span>                           |
| <span data-ttu-id="b13bb-281">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="b13bb-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="b13bb-282">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="b13bb-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b13bb-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b13bb-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b13bb-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b13bb-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b13bb-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b13bb-285">Search-Flags</span></span>           | <span data-ttu-id="b13bb-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b13bb-286">0x00000000</span></span>                      |
| <span data-ttu-id="b13bb-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b13bb-287">System-Flags</span></span>           | <span data-ttu-id="b13bb-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b13bb-288">0x00000010</span></span>                      |
| <span data-ttu-id="b13bb-289">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="b13bb-289">Classes used in</span></span>        | [<span data-ttu-id="b13bb-290">**Início**</span><span class="sxs-lookup"><span data-stu-id="b13bb-290">**Top**</span></span>](c-top.md)<br/> |



 

 





