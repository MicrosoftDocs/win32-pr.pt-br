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
# <a name="ms-ds-consistency-guid-attribute"></a><span data-ttu-id="af4dd-105">Atributo MS-DS-Consistency-GUID</span><span class="sxs-lookup"><span data-stu-id="af4dd-105">MS-DS-Consistency-Guid attribute</span></span>

<span data-ttu-id="af4dd-106">Esse atributo é usado para verificar a consistência entre o diretório e outro objeto, banco de dados ou aplicativo, comparando GUIDs.</span><span class="sxs-lookup"><span data-stu-id="af4dd-106">This attribute is used to check consistency between the directory and another object, database, or application, by comparing GUIDs.</span></span>



| <span data-ttu-id="af4dd-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="af4dd-107">Entry</span></span> | <span data-ttu-id="af4dd-108">Valor</span><span class="sxs-lookup"><span data-stu-id="af4dd-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="af4dd-109">CN</span><span class="sxs-lookup"><span data-stu-id="af4dd-109">CN</span></span>                | <span data-ttu-id="af4dd-110">MS-DS-Consistency-Guid</span><span class="sxs-lookup"><span data-stu-id="af4dd-110">MS-DS-Consistency-Guid</span></span>                                |
| <span data-ttu-id="af4dd-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="af4dd-111">Ldap-Display-Name</span></span> | <span data-ttu-id="af4dd-112">mS-DS-ConsistencyGuid</span><span class="sxs-lookup"><span data-stu-id="af4dd-112">mS-DS-ConsistencyGuid</span></span>                                 |
| <span data-ttu-id="af4dd-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="af4dd-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="af4dd-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="af4dd-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="af4dd-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="af4dd-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="af4dd-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="af4dd-116">Attribute-Id</span></span>      | <span data-ttu-id="af4dd-117">1.2.840.113556.1.4.1360</span><span class="sxs-lookup"><span data-stu-id="af4dd-117">1.2.840.113556.1.4.1360</span></span>                               |
| <span data-ttu-id="af4dd-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="af4dd-118">System-Id-Guid</span></span>    | <span data-ttu-id="af4dd-119">23773dc2-b63a-11d2-90e1-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="af4dd-119">23773dc2-b63a-11d2-90e1-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="af4dd-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="af4dd-120">Syntax</span></span>            | [<span data-ttu-id="af4dd-121">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="af4dd-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="af4dd-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="af4dd-122">Implementations</span></span>

-   [<span data-ttu-id="af4dd-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="af4dd-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="af4dd-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="af4dd-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="af4dd-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="af4dd-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="af4dd-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="af4dd-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="af4dd-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="af4dd-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="af4dd-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="af4dd-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="af4dd-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="af4dd-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="af4dd-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="af4dd-130">Windows 2000 Server</span></span>



| <span data-ttu-id="af4dd-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="af4dd-131">Entry</span></span> | <span data-ttu-id="af4dd-132">Valor</span><span class="sxs-lookup"><span data-stu-id="af4dd-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="af4dd-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="af4dd-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="af4dd-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af4dd-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="af4dd-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="af4dd-135">System-Only</span></span>            | <span data-ttu-id="af4dd-136">Falso</span><span class="sxs-lookup"><span data-stu-id="af4dd-136">False</span></span>                           |
| <span data-ttu-id="af4dd-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="af4dd-137">Is-Single-Valued</span></span>       | <span data-ttu-id="af4dd-138">True</span><span class="sxs-lookup"><span data-stu-id="af4dd-138">True</span></span>                            |
| <span data-ttu-id="af4dd-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="af4dd-139">Is Indexed</span></span>             | <span data-ttu-id="af4dd-140">Falso</span><span class="sxs-lookup"><span data-stu-id="af4dd-140">False</span></span>                           |
| <span data-ttu-id="af4dd-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="af4dd-141">In Global Catalog</span></span>      | <span data-ttu-id="af4dd-142">Falso</span><span class="sxs-lookup"><span data-stu-id="af4dd-142">False</span></span>                           |
| <span data-ttu-id="af4dd-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="af4dd-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="af4dd-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="af4dd-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="af4dd-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af4dd-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="af4dd-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af4dd-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="af4dd-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af4dd-147">Search-Flags</span></span>           | <span data-ttu-id="af4dd-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af4dd-148">0x00000000</span></span>                      |
| <span data-ttu-id="af4dd-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af4dd-149">System-Flags</span></span>           | <span data-ttu-id="af4dd-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af4dd-150">0x00000010</span></span>                      |
| <span data-ttu-id="af4dd-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="af4dd-151">Classes used in</span></span>        | [<span data-ttu-id="af4dd-152">**Início**</span><span class="sxs-lookup"><span data-stu-id="af4dd-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="af4dd-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="af4dd-153">Windows Server 2003</span></span>



| <span data-ttu-id="af4dd-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="af4dd-154">Entry</span></span> | <span data-ttu-id="af4dd-155">Valor</span><span class="sxs-lookup"><span data-stu-id="af4dd-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="af4dd-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="af4dd-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="af4dd-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af4dd-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="af4dd-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="af4dd-158">System-Only</span></span>            | <span data-ttu-id="af4dd-159">Falso</span><span class="sxs-lookup"><span data-stu-id="af4dd-159">False</span></span>                           |
| <span data-ttu-id="af4dd-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="af4dd-160">Is-Single-Valued</span></span>       | <span data-ttu-id="af4dd-161">True</span><span class="sxs-lookup"><span data-stu-id="af4dd-161">True</span></span>                            |
| <span data-ttu-id="af4dd-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="af4dd-162">Is Indexed</span></span>             | <span data-ttu-id="af4dd-163">Falso</span><span class="sxs-lookup"><span data-stu-id="af4dd-163">False</span></span>                           |
| <span data-ttu-id="af4dd-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="af4dd-164">In Global Catalog</span></span>      | <span data-ttu-id="af4dd-165">Falso</span><span class="sxs-lookup"><span data-stu-id="af4dd-165">False</span></span>                           |
| <span data-ttu-id="af4dd-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="af4dd-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="af4dd-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="af4dd-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="af4dd-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af4dd-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="af4dd-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af4dd-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="af4dd-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af4dd-170">Search-Flags</span></span>           | <span data-ttu-id="af4dd-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af4dd-171">0x00000000</span></span>                      |
| <span data-ttu-id="af4dd-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af4dd-172">System-Flags</span></span>           | <span data-ttu-id="af4dd-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af4dd-173">0x00000010</span></span>                      |
| <span data-ttu-id="af4dd-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="af4dd-174">Classes used in</span></span>        | [<span data-ttu-id="af4dd-175">**Início**</span><span class="sxs-lookup"><span data-stu-id="af4dd-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="af4dd-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="af4dd-176">ADAM</span></span>



| <span data-ttu-id="af4dd-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="af4dd-177">Entry</span></span> | <span data-ttu-id="af4dd-178">Valor</span><span class="sxs-lookup"><span data-stu-id="af4dd-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="af4dd-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="af4dd-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="af4dd-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af4dd-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="af4dd-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="af4dd-181">System-Only</span></span>            | <span data-ttu-id="af4dd-182">Falso</span><span class="sxs-lookup"><span data-stu-id="af4dd-182">False</span></span>                           |
| <span data-ttu-id="af4dd-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="af4dd-183">Is-Single-Valued</span></span>       | <span data-ttu-id="af4dd-184">True</span><span class="sxs-lookup"><span data-stu-id="af4dd-184">True</span></span>                            |
| <span data-ttu-id="af4dd-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="af4dd-185">Is Indexed</span></span>             | <span data-ttu-id="af4dd-186">Falso</span><span class="sxs-lookup"><span data-stu-id="af4dd-186">False</span></span>                           |
| <span data-ttu-id="af4dd-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="af4dd-187">In Global Catalog</span></span>      | <span data-ttu-id="af4dd-188">Falso</span><span class="sxs-lookup"><span data-stu-id="af4dd-188">False</span></span>                           |
| <span data-ttu-id="af4dd-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="af4dd-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="af4dd-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="af4dd-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="af4dd-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af4dd-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="af4dd-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af4dd-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="af4dd-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af4dd-193">Search-Flags</span></span>           | <span data-ttu-id="af4dd-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af4dd-194">0x00000000</span></span>                      |
| <span data-ttu-id="af4dd-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af4dd-195">System-Flags</span></span>           | <span data-ttu-id="af4dd-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af4dd-196">0x00000010</span></span>                      |
| <span data-ttu-id="af4dd-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="af4dd-197">Classes used in</span></span>        | [<span data-ttu-id="af4dd-198">**Início**</span><span class="sxs-lookup"><span data-stu-id="af4dd-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="af4dd-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="af4dd-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="af4dd-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="af4dd-200">Entry</span></span> | <span data-ttu-id="af4dd-201">Valor</span><span class="sxs-lookup"><span data-stu-id="af4dd-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="af4dd-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="af4dd-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="af4dd-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af4dd-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="af4dd-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="af4dd-204">System-Only</span></span>            | <span data-ttu-id="af4dd-205">Falso</span><span class="sxs-lookup"><span data-stu-id="af4dd-205">False</span></span>                           |
| <span data-ttu-id="af4dd-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="af4dd-206">Is-Single-Valued</span></span>       | <span data-ttu-id="af4dd-207">True</span><span class="sxs-lookup"><span data-stu-id="af4dd-207">True</span></span>                            |
| <span data-ttu-id="af4dd-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="af4dd-208">Is Indexed</span></span>             | <span data-ttu-id="af4dd-209">Falso</span><span class="sxs-lookup"><span data-stu-id="af4dd-209">False</span></span>                           |
| <span data-ttu-id="af4dd-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="af4dd-210">In Global Catalog</span></span>      | <span data-ttu-id="af4dd-211">Falso</span><span class="sxs-lookup"><span data-stu-id="af4dd-211">False</span></span>                           |
| <span data-ttu-id="af4dd-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="af4dd-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="af4dd-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="af4dd-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="af4dd-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af4dd-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="af4dd-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af4dd-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="af4dd-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af4dd-216">Search-Flags</span></span>           | <span data-ttu-id="af4dd-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af4dd-217">0x00000000</span></span>                      |
| <span data-ttu-id="af4dd-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af4dd-218">System-Flags</span></span>           | <span data-ttu-id="af4dd-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af4dd-219">0x00000010</span></span>                      |
| <span data-ttu-id="af4dd-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="af4dd-220">Classes used in</span></span>        | [<span data-ttu-id="af4dd-221">**Início**</span><span class="sxs-lookup"><span data-stu-id="af4dd-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="af4dd-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af4dd-222">Windows Server 2008</span></span>



| <span data-ttu-id="af4dd-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="af4dd-223">Entry</span></span> | <span data-ttu-id="af4dd-224">Valor</span><span class="sxs-lookup"><span data-stu-id="af4dd-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="af4dd-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="af4dd-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="af4dd-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af4dd-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="af4dd-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="af4dd-227">System-Only</span></span>            | <span data-ttu-id="af4dd-228">Falso</span><span class="sxs-lookup"><span data-stu-id="af4dd-228">False</span></span>                           |
| <span data-ttu-id="af4dd-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="af4dd-229">Is-Single-Valued</span></span>       | <span data-ttu-id="af4dd-230">True</span><span class="sxs-lookup"><span data-stu-id="af4dd-230">True</span></span>                            |
| <span data-ttu-id="af4dd-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="af4dd-231">Is Indexed</span></span>             | <span data-ttu-id="af4dd-232">Falso</span><span class="sxs-lookup"><span data-stu-id="af4dd-232">False</span></span>                           |
| <span data-ttu-id="af4dd-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="af4dd-233">In Global Catalog</span></span>      | <span data-ttu-id="af4dd-234">Falso</span><span class="sxs-lookup"><span data-stu-id="af4dd-234">False</span></span>                           |
| <span data-ttu-id="af4dd-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="af4dd-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="af4dd-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="af4dd-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="af4dd-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af4dd-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="af4dd-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af4dd-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="af4dd-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af4dd-239">Search-Flags</span></span>           | <span data-ttu-id="af4dd-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af4dd-240">0x00000000</span></span>                      |
| <span data-ttu-id="af4dd-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af4dd-241">System-Flags</span></span>           | <span data-ttu-id="af4dd-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af4dd-242">0x00000010</span></span>                      |
| <span data-ttu-id="af4dd-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="af4dd-243">Classes used in</span></span>        | [<span data-ttu-id="af4dd-244">**Início**</span><span class="sxs-lookup"><span data-stu-id="af4dd-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="af4dd-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="af4dd-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="af4dd-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="af4dd-246">Entry</span></span> | <span data-ttu-id="af4dd-247">Valor</span><span class="sxs-lookup"><span data-stu-id="af4dd-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="af4dd-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="af4dd-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="af4dd-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af4dd-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="af4dd-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="af4dd-250">System-Only</span></span>            | <span data-ttu-id="af4dd-251">Falso</span><span class="sxs-lookup"><span data-stu-id="af4dd-251">False</span></span>                           |
| <span data-ttu-id="af4dd-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="af4dd-252">Is-Single-Valued</span></span>       | <span data-ttu-id="af4dd-253">True</span><span class="sxs-lookup"><span data-stu-id="af4dd-253">True</span></span>                            |
| <span data-ttu-id="af4dd-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="af4dd-254">Is Indexed</span></span>             | <span data-ttu-id="af4dd-255">Falso</span><span class="sxs-lookup"><span data-stu-id="af4dd-255">False</span></span>                           |
| <span data-ttu-id="af4dd-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="af4dd-256">In Global Catalog</span></span>      | <span data-ttu-id="af4dd-257">Falso</span><span class="sxs-lookup"><span data-stu-id="af4dd-257">False</span></span>                           |
| <span data-ttu-id="af4dd-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="af4dd-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="af4dd-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="af4dd-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="af4dd-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af4dd-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="af4dd-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af4dd-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="af4dd-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af4dd-262">Search-Flags</span></span>           | <span data-ttu-id="af4dd-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af4dd-263">0x00000000</span></span>                      |
| <span data-ttu-id="af4dd-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af4dd-264">System-Flags</span></span>           | <span data-ttu-id="af4dd-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af4dd-265">0x00000010</span></span>                      |
| <span data-ttu-id="af4dd-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="af4dd-266">Classes used in</span></span>        | [<span data-ttu-id="af4dd-267">**Início**</span><span class="sxs-lookup"><span data-stu-id="af4dd-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="af4dd-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="af4dd-268">Windows Server 2012</span></span>



| <span data-ttu-id="af4dd-269">Entrada</span><span class="sxs-lookup"><span data-stu-id="af4dd-269">Entry</span></span> | <span data-ttu-id="af4dd-270">Valor</span><span class="sxs-lookup"><span data-stu-id="af4dd-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="af4dd-271">ID do link</span><span class="sxs-lookup"><span data-stu-id="af4dd-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="af4dd-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af4dd-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="af4dd-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="af4dd-273">System-Only</span></span>            | <span data-ttu-id="af4dd-274">Falso</span><span class="sxs-lookup"><span data-stu-id="af4dd-274">False</span></span>                           |
| <span data-ttu-id="af4dd-275">É de valor único</span><span class="sxs-lookup"><span data-stu-id="af4dd-275">Is-Single-Valued</span></span>       | <span data-ttu-id="af4dd-276">True</span><span class="sxs-lookup"><span data-stu-id="af4dd-276">True</span></span>                            |
| <span data-ttu-id="af4dd-277">É indexado</span><span class="sxs-lookup"><span data-stu-id="af4dd-277">Is Indexed</span></span>             | <span data-ttu-id="af4dd-278">Falso</span><span class="sxs-lookup"><span data-stu-id="af4dd-278">False</span></span>                           |
| <span data-ttu-id="af4dd-279">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="af4dd-279">In Global Catalog</span></span>      | <span data-ttu-id="af4dd-280">Falso</span><span class="sxs-lookup"><span data-stu-id="af4dd-280">False</span></span>                           |
| <span data-ttu-id="af4dd-281">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="af4dd-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="af4dd-282">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="af4dd-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="af4dd-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af4dd-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="af4dd-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af4dd-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="af4dd-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af4dd-285">Search-Flags</span></span>           | <span data-ttu-id="af4dd-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af4dd-286">0x00000000</span></span>                      |
| <span data-ttu-id="af4dd-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af4dd-287">System-Flags</span></span>           | <span data-ttu-id="af4dd-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af4dd-288">0x00000010</span></span>                      |
| <span data-ttu-id="af4dd-289">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="af4dd-289">Classes used in</span></span>        | [<span data-ttu-id="af4dd-290">**Início**</span><span class="sxs-lookup"><span data-stu-id="af4dd-290">**Top**</span></span>](c-top.md)<br/> |



 

 





