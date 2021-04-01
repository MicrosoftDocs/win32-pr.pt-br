---
title: Object-Guid atributo
description: O identificador exclusivo de um objeto.
ms.assetid: fc2d65a3-7472-41ef-9780-d1a7ec965804
ms.tgt_platform: multiple
keywords:
- Esquema de Object-Guid do atributo AD
- Esquema do AD do atributo objectGUID
topic_type:
- apiref
api_name:
- Object-Guid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07e3715c38b629869296e6f8df5dbebd9a515d1b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825309"
---
# <a name="object-guid-attribute"></a><span data-ttu-id="652c5-105">Object-Guid atributo</span><span class="sxs-lookup"><span data-stu-id="652c5-105">Object-Guid attribute</span></span>

<span data-ttu-id="652c5-106">O identificador exclusivo de um objeto.</span><span class="sxs-lookup"><span data-stu-id="652c5-106">The unique identifier for an object.</span></span>



| <span data-ttu-id="652c5-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="652c5-107">Entry</span></span> | <span data-ttu-id="652c5-108">Valor</span><span class="sxs-lookup"><span data-stu-id="652c5-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------|
| <span data-ttu-id="652c5-109">CN</span><span class="sxs-lookup"><span data-stu-id="652c5-109">CN</span></span>                | <span data-ttu-id="652c5-110">Object-Guid</span><span class="sxs-lookup"><span data-stu-id="652c5-110">Object-Guid</span></span>                                                         |
| <span data-ttu-id="652c5-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="652c5-111">Ldap-Display-Name</span></span> | <span data-ttu-id="652c5-112">objectGUID</span><span class="sxs-lookup"><span data-stu-id="652c5-112">objectGUID</span></span>                                                          |
| <span data-ttu-id="652c5-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="652c5-113">Size</span></span>              | <span data-ttu-id="652c5-114">16 bytes</span><span class="sxs-lookup"><span data-stu-id="652c5-114">16 bytes</span></span>                                                            |
| <span data-ttu-id="652c5-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="652c5-115">Update Privilege</span></span>  | <span data-ttu-id="652c5-116">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="652c5-116">This value is set by the system.</span></span>                                    |
| <span data-ttu-id="652c5-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="652c5-117">Update Frequency</span></span>  | <span data-ttu-id="652c5-118">Esse valor é definido quando o objeto é criado e não pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="652c5-118">This value is set when the object is created and cannot be changed.</span></span> |
| <span data-ttu-id="652c5-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="652c5-119">Attribute-Id</span></span>      | <span data-ttu-id="652c5-120">1.2.840.113556.1.4.2</span><span class="sxs-lookup"><span data-stu-id="652c5-120">1.2.840.113556.1.4.2</span></span>                                                |
| <span data-ttu-id="652c5-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="652c5-121">System-Id-Guid</span></span>    | <span data-ttu-id="652c5-122">bf9679e7-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="652c5-122">bf9679e7-0de6-11d0-a285-00aa003049e2</span></span>                                |
| <span data-ttu-id="652c5-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="652c5-123">Syntax</span></span>            | [<span data-ttu-id="652c5-124">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="652c5-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)               |



## <a name="implementations"></a><span data-ttu-id="652c5-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="652c5-125">Implementations</span></span>

-   [<span data-ttu-id="652c5-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="652c5-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="652c5-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="652c5-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="652c5-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="652c5-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="652c5-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="652c5-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="652c5-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="652c5-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="652c5-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="652c5-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="652c5-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="652c5-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="652c5-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="652c5-133">Windows 2000 Server</span></span>



| <span data-ttu-id="652c5-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="652c5-134">Entry</span></span> | <span data-ttu-id="652c5-135">Valor</span><span class="sxs-lookup"><span data-stu-id="652c5-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="652c5-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="652c5-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="652c5-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="652c5-137">MAPI-Id</span></span>                | <span data-ttu-id="652c5-138">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="652c5-138">0x8C6D</span></span>                          |
| <span data-ttu-id="652c5-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="652c5-139">System-Only</span></span>            | <span data-ttu-id="652c5-140">True</span><span class="sxs-lookup"><span data-stu-id="652c5-140">True</span></span>                            |
| <span data-ttu-id="652c5-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="652c5-141">Is-Single-Valued</span></span>       | <span data-ttu-id="652c5-142">True</span><span class="sxs-lookup"><span data-stu-id="652c5-142">True</span></span>                            |
| <span data-ttu-id="652c5-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="652c5-143">Is Indexed</span></span>             | <span data-ttu-id="652c5-144">True</span><span class="sxs-lookup"><span data-stu-id="652c5-144">True</span></span>                            |
| <span data-ttu-id="652c5-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="652c5-145">In Global Catalog</span></span>      | <span data-ttu-id="652c5-146">True</span><span class="sxs-lookup"><span data-stu-id="652c5-146">True</span></span>                            |
| <span data-ttu-id="652c5-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="652c5-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="652c5-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="652c5-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="652c5-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="652c5-149">Range-Lower</span></span>            | <span data-ttu-id="652c5-150">16</span><span class="sxs-lookup"><span data-stu-id="652c5-150">16</span></span>                              |
| <span data-ttu-id="652c5-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="652c5-151">Range-Upper</span></span>            | <span data-ttu-id="652c5-152">16</span><span class="sxs-lookup"><span data-stu-id="652c5-152">16</span></span>                              |
| <span data-ttu-id="652c5-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="652c5-153">Search-Flags</span></span>           | <span data-ttu-id="652c5-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="652c5-154">0x00000009</span></span>                      |
| <span data-ttu-id="652c5-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="652c5-155">System-Flags</span></span>           | <span data-ttu-id="652c5-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="652c5-156">0x00000013</span></span>                      |
| <span data-ttu-id="652c5-157">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="652c5-157">Classes used in</span></span>        | [<span data-ttu-id="652c5-158">**Início**</span><span class="sxs-lookup"><span data-stu-id="652c5-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="652c5-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="652c5-159">Windows Server 2003</span></span>



| <span data-ttu-id="652c5-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="652c5-160">Entry</span></span> | <span data-ttu-id="652c5-161">Valor</span><span class="sxs-lookup"><span data-stu-id="652c5-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="652c5-162">ID do link</span><span class="sxs-lookup"><span data-stu-id="652c5-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="652c5-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="652c5-163">MAPI-Id</span></span>                | <span data-ttu-id="652c5-164">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="652c5-164">0x8C6D</span></span>                          |
| <span data-ttu-id="652c5-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="652c5-165">System-Only</span></span>            | <span data-ttu-id="652c5-166">True</span><span class="sxs-lookup"><span data-stu-id="652c5-166">True</span></span>                            |
| <span data-ttu-id="652c5-167">É de valor único</span><span class="sxs-lookup"><span data-stu-id="652c5-167">Is-Single-Valued</span></span>       | <span data-ttu-id="652c5-168">True</span><span class="sxs-lookup"><span data-stu-id="652c5-168">True</span></span>                            |
| <span data-ttu-id="652c5-169">É indexado</span><span class="sxs-lookup"><span data-stu-id="652c5-169">Is Indexed</span></span>             | <span data-ttu-id="652c5-170">True</span><span class="sxs-lookup"><span data-stu-id="652c5-170">True</span></span>                            |
| <span data-ttu-id="652c5-171">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="652c5-171">In Global Catalog</span></span>      | <span data-ttu-id="652c5-172">True</span><span class="sxs-lookup"><span data-stu-id="652c5-172">True</span></span>                            |
| <span data-ttu-id="652c5-173">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="652c5-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="652c5-174">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="652c5-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="652c5-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="652c5-175">Range-Lower</span></span>            | <span data-ttu-id="652c5-176">16</span><span class="sxs-lookup"><span data-stu-id="652c5-176">16</span></span>                              |
| <span data-ttu-id="652c5-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="652c5-177">Range-Upper</span></span>            | <span data-ttu-id="652c5-178">16</span><span class="sxs-lookup"><span data-stu-id="652c5-178">16</span></span>                              |
| <span data-ttu-id="652c5-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="652c5-179">Search-Flags</span></span>           | <span data-ttu-id="652c5-180">0x00000009</span><span class="sxs-lookup"><span data-stu-id="652c5-180">0x00000009</span></span>                      |
| <span data-ttu-id="652c5-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="652c5-181">System-Flags</span></span>           | <span data-ttu-id="652c5-182">0x00000013</span><span class="sxs-lookup"><span data-stu-id="652c5-182">0x00000013</span></span>                      |
| <span data-ttu-id="652c5-183">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="652c5-183">Classes used in</span></span>        | [<span data-ttu-id="652c5-184">**Início**</span><span class="sxs-lookup"><span data-stu-id="652c5-184">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="652c5-185">ADAM</span><span class="sxs-lookup"><span data-stu-id="652c5-185">ADAM</span></span>



| <span data-ttu-id="652c5-186">Entrada</span><span class="sxs-lookup"><span data-stu-id="652c5-186">Entry</span></span> | <span data-ttu-id="652c5-187">Valor</span><span class="sxs-lookup"><span data-stu-id="652c5-187">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="652c5-188">ID do link</span><span class="sxs-lookup"><span data-stu-id="652c5-188">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="652c5-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="652c5-189">MAPI-Id</span></span>                | <span data-ttu-id="652c5-190">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="652c5-190">0x8C6D</span></span>                          |
| <span data-ttu-id="652c5-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="652c5-191">System-Only</span></span>            | <span data-ttu-id="652c5-192">True</span><span class="sxs-lookup"><span data-stu-id="652c5-192">True</span></span>                            |
| <span data-ttu-id="652c5-193">É de valor único</span><span class="sxs-lookup"><span data-stu-id="652c5-193">Is-Single-Valued</span></span>       | <span data-ttu-id="652c5-194">True</span><span class="sxs-lookup"><span data-stu-id="652c5-194">True</span></span>                            |
| <span data-ttu-id="652c5-195">É indexado</span><span class="sxs-lookup"><span data-stu-id="652c5-195">Is Indexed</span></span>             | <span data-ttu-id="652c5-196">True</span><span class="sxs-lookup"><span data-stu-id="652c5-196">True</span></span>                            |
| <span data-ttu-id="652c5-197">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="652c5-197">In Global Catalog</span></span>      | <span data-ttu-id="652c5-198">True</span><span class="sxs-lookup"><span data-stu-id="652c5-198">True</span></span>                            |
| <span data-ttu-id="652c5-199">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="652c5-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="652c5-200">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="652c5-200">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="652c5-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="652c5-201">Range-Lower</span></span>            | <span data-ttu-id="652c5-202">16</span><span class="sxs-lookup"><span data-stu-id="652c5-202">16</span></span>                              |
| <span data-ttu-id="652c5-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="652c5-203">Range-Upper</span></span>            | <span data-ttu-id="652c5-204">16</span><span class="sxs-lookup"><span data-stu-id="652c5-204">16</span></span>                              |
| <span data-ttu-id="652c5-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="652c5-205">Search-Flags</span></span>           | <span data-ttu-id="652c5-206">0x00000009</span><span class="sxs-lookup"><span data-stu-id="652c5-206">0x00000009</span></span>                      |
| <span data-ttu-id="652c5-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="652c5-207">System-Flags</span></span>           | <span data-ttu-id="652c5-208">0x00000013</span><span class="sxs-lookup"><span data-stu-id="652c5-208">0x00000013</span></span>                      |
| <span data-ttu-id="652c5-209">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="652c5-209">Classes used in</span></span>        | [<span data-ttu-id="652c5-210">**Início**</span><span class="sxs-lookup"><span data-stu-id="652c5-210">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="652c5-211">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="652c5-211">Windows Server 2003 R2</span></span>



| <span data-ttu-id="652c5-212">Entrada</span><span class="sxs-lookup"><span data-stu-id="652c5-212">Entry</span></span> | <span data-ttu-id="652c5-213">Valor</span><span class="sxs-lookup"><span data-stu-id="652c5-213">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="652c5-214">ID do link</span><span class="sxs-lookup"><span data-stu-id="652c5-214">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="652c5-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="652c5-215">MAPI-Id</span></span>                | <span data-ttu-id="652c5-216">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="652c5-216">0x8C6D</span></span>                          |
| <span data-ttu-id="652c5-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="652c5-217">System-Only</span></span>            | <span data-ttu-id="652c5-218">True</span><span class="sxs-lookup"><span data-stu-id="652c5-218">True</span></span>                            |
| <span data-ttu-id="652c5-219">É de valor único</span><span class="sxs-lookup"><span data-stu-id="652c5-219">Is-Single-Valued</span></span>       | <span data-ttu-id="652c5-220">True</span><span class="sxs-lookup"><span data-stu-id="652c5-220">True</span></span>                            |
| <span data-ttu-id="652c5-221">É indexado</span><span class="sxs-lookup"><span data-stu-id="652c5-221">Is Indexed</span></span>             | <span data-ttu-id="652c5-222">True</span><span class="sxs-lookup"><span data-stu-id="652c5-222">True</span></span>                            |
| <span data-ttu-id="652c5-223">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="652c5-223">In Global Catalog</span></span>      | <span data-ttu-id="652c5-224">True</span><span class="sxs-lookup"><span data-stu-id="652c5-224">True</span></span>                            |
| <span data-ttu-id="652c5-225">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="652c5-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="652c5-226">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="652c5-226">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="652c5-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="652c5-227">Range-Lower</span></span>            | <span data-ttu-id="652c5-228">16</span><span class="sxs-lookup"><span data-stu-id="652c5-228">16</span></span>                              |
| <span data-ttu-id="652c5-229">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="652c5-229">Range-Upper</span></span>            | <span data-ttu-id="652c5-230">16</span><span class="sxs-lookup"><span data-stu-id="652c5-230">16</span></span>                              |
| <span data-ttu-id="652c5-231">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="652c5-231">Search-Flags</span></span>           | <span data-ttu-id="652c5-232">0x00000009</span><span class="sxs-lookup"><span data-stu-id="652c5-232">0x00000009</span></span>                      |
| <span data-ttu-id="652c5-233">System-Flags</span><span class="sxs-lookup"><span data-stu-id="652c5-233">System-Flags</span></span>           | <span data-ttu-id="652c5-234">0x00000013</span><span class="sxs-lookup"><span data-stu-id="652c5-234">0x00000013</span></span>                      |
| <span data-ttu-id="652c5-235">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="652c5-235">Classes used in</span></span>        | [<span data-ttu-id="652c5-236">**Início**</span><span class="sxs-lookup"><span data-stu-id="652c5-236">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="652c5-237">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="652c5-237">Windows Server 2008</span></span>



| <span data-ttu-id="652c5-238">Entrada</span><span class="sxs-lookup"><span data-stu-id="652c5-238">Entry</span></span> | <span data-ttu-id="652c5-239">Valor</span><span class="sxs-lookup"><span data-stu-id="652c5-239">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="652c5-240">ID do link</span><span class="sxs-lookup"><span data-stu-id="652c5-240">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="652c5-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="652c5-241">MAPI-Id</span></span>                | <span data-ttu-id="652c5-242">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="652c5-242">0x8C6D</span></span>                          |
| <span data-ttu-id="652c5-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="652c5-243">System-Only</span></span>            | <span data-ttu-id="652c5-244">True</span><span class="sxs-lookup"><span data-stu-id="652c5-244">True</span></span>                            |
| <span data-ttu-id="652c5-245">É de valor único</span><span class="sxs-lookup"><span data-stu-id="652c5-245">Is-Single-Valued</span></span>       | <span data-ttu-id="652c5-246">True</span><span class="sxs-lookup"><span data-stu-id="652c5-246">True</span></span>                            |
| <span data-ttu-id="652c5-247">É indexado</span><span class="sxs-lookup"><span data-stu-id="652c5-247">Is Indexed</span></span>             | <span data-ttu-id="652c5-248">True</span><span class="sxs-lookup"><span data-stu-id="652c5-248">True</span></span>                            |
| <span data-ttu-id="652c5-249">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="652c5-249">In Global Catalog</span></span>      | <span data-ttu-id="652c5-250">True</span><span class="sxs-lookup"><span data-stu-id="652c5-250">True</span></span>                            |
| <span data-ttu-id="652c5-251">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="652c5-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="652c5-252">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="652c5-252">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="652c5-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="652c5-253">Range-Lower</span></span>            | <span data-ttu-id="652c5-254">16</span><span class="sxs-lookup"><span data-stu-id="652c5-254">16</span></span>                              |
| <span data-ttu-id="652c5-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="652c5-255">Range-Upper</span></span>            | <span data-ttu-id="652c5-256">16</span><span class="sxs-lookup"><span data-stu-id="652c5-256">16</span></span>                              |
| <span data-ttu-id="652c5-257">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="652c5-257">Search-Flags</span></span>           | <span data-ttu-id="652c5-258">0x00000009</span><span class="sxs-lookup"><span data-stu-id="652c5-258">0x00000009</span></span>                      |
| <span data-ttu-id="652c5-259">System-Flags</span><span class="sxs-lookup"><span data-stu-id="652c5-259">System-Flags</span></span>           | <span data-ttu-id="652c5-260">0x00000013</span><span class="sxs-lookup"><span data-stu-id="652c5-260">0x00000013</span></span>                      |
| <span data-ttu-id="652c5-261">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="652c5-261">Classes used in</span></span>        | [<span data-ttu-id="652c5-262">**Início**</span><span class="sxs-lookup"><span data-stu-id="652c5-262">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="652c5-263">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="652c5-263">Windows Server 2008 R2</span></span>



| <span data-ttu-id="652c5-264">Entrada</span><span class="sxs-lookup"><span data-stu-id="652c5-264">Entry</span></span> | <span data-ttu-id="652c5-265">Valor</span><span class="sxs-lookup"><span data-stu-id="652c5-265">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="652c5-266">ID do link</span><span class="sxs-lookup"><span data-stu-id="652c5-266">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="652c5-267">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="652c5-267">MAPI-Id</span></span>                | <span data-ttu-id="652c5-268">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="652c5-268">0x8C6D</span></span>                          |
| <span data-ttu-id="652c5-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="652c5-269">System-Only</span></span>            | <span data-ttu-id="652c5-270">True</span><span class="sxs-lookup"><span data-stu-id="652c5-270">True</span></span>                            |
| <span data-ttu-id="652c5-271">É de valor único</span><span class="sxs-lookup"><span data-stu-id="652c5-271">Is-Single-Valued</span></span>       | <span data-ttu-id="652c5-272">True</span><span class="sxs-lookup"><span data-stu-id="652c5-272">True</span></span>                            |
| <span data-ttu-id="652c5-273">É indexado</span><span class="sxs-lookup"><span data-stu-id="652c5-273">Is Indexed</span></span>             | <span data-ttu-id="652c5-274">True</span><span class="sxs-lookup"><span data-stu-id="652c5-274">True</span></span>                            |
| <span data-ttu-id="652c5-275">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="652c5-275">In Global Catalog</span></span>      | <span data-ttu-id="652c5-276">True</span><span class="sxs-lookup"><span data-stu-id="652c5-276">True</span></span>                            |
| <span data-ttu-id="652c5-277">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="652c5-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="652c5-278">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="652c5-278">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="652c5-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="652c5-279">Range-Lower</span></span>            | <span data-ttu-id="652c5-280">16</span><span class="sxs-lookup"><span data-stu-id="652c5-280">16</span></span>                              |
| <span data-ttu-id="652c5-281">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="652c5-281">Range-Upper</span></span>            | <span data-ttu-id="652c5-282">16</span><span class="sxs-lookup"><span data-stu-id="652c5-282">16</span></span>                              |
| <span data-ttu-id="652c5-283">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="652c5-283">Search-Flags</span></span>           | <span data-ttu-id="652c5-284">0x00000009</span><span class="sxs-lookup"><span data-stu-id="652c5-284">0x00000009</span></span>                      |
| <span data-ttu-id="652c5-285">System-Flags</span><span class="sxs-lookup"><span data-stu-id="652c5-285">System-Flags</span></span>           | <span data-ttu-id="652c5-286">0x00000013</span><span class="sxs-lookup"><span data-stu-id="652c5-286">0x00000013</span></span>                      |
| <span data-ttu-id="652c5-287">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="652c5-287">Classes used in</span></span>        | [<span data-ttu-id="652c5-288">**Início**</span><span class="sxs-lookup"><span data-stu-id="652c5-288">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="652c5-289">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="652c5-289">Windows Server 2012</span></span>



| <span data-ttu-id="652c5-290">Entrada</span><span class="sxs-lookup"><span data-stu-id="652c5-290">Entry</span></span> | <span data-ttu-id="652c5-291">Valor</span><span class="sxs-lookup"><span data-stu-id="652c5-291">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="652c5-292">ID do link</span><span class="sxs-lookup"><span data-stu-id="652c5-292">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="652c5-293">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="652c5-293">MAPI-Id</span></span>                | <span data-ttu-id="652c5-294">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="652c5-294">0x8C6D</span></span>                          |
| <span data-ttu-id="652c5-295">System-Only</span><span class="sxs-lookup"><span data-stu-id="652c5-295">System-Only</span></span>            | <span data-ttu-id="652c5-296">True</span><span class="sxs-lookup"><span data-stu-id="652c5-296">True</span></span>                            |
| <span data-ttu-id="652c5-297">É de valor único</span><span class="sxs-lookup"><span data-stu-id="652c5-297">Is-Single-Valued</span></span>       | <span data-ttu-id="652c5-298">True</span><span class="sxs-lookup"><span data-stu-id="652c5-298">True</span></span>                            |
| <span data-ttu-id="652c5-299">É indexado</span><span class="sxs-lookup"><span data-stu-id="652c5-299">Is Indexed</span></span>             | <span data-ttu-id="652c5-300">True</span><span class="sxs-lookup"><span data-stu-id="652c5-300">True</span></span>                            |
| <span data-ttu-id="652c5-301">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="652c5-301">In Global Catalog</span></span>      | <span data-ttu-id="652c5-302">True</span><span class="sxs-lookup"><span data-stu-id="652c5-302">True</span></span>                            |
| <span data-ttu-id="652c5-303">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="652c5-303">NT-Security-Descriptor</span></span> | <span data-ttu-id="652c5-304">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="652c5-304">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="652c5-305">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="652c5-305">Range-Lower</span></span>            | <span data-ttu-id="652c5-306">16</span><span class="sxs-lookup"><span data-stu-id="652c5-306">16</span></span>                              |
| <span data-ttu-id="652c5-307">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="652c5-307">Range-Upper</span></span>            | <span data-ttu-id="652c5-308">16</span><span class="sxs-lookup"><span data-stu-id="652c5-308">16</span></span>                              |
| <span data-ttu-id="652c5-309">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="652c5-309">Search-Flags</span></span>           | <span data-ttu-id="652c5-310">0x00000009</span><span class="sxs-lookup"><span data-stu-id="652c5-310">0x00000009</span></span>                      |
| <span data-ttu-id="652c5-311">System-Flags</span><span class="sxs-lookup"><span data-stu-id="652c5-311">System-Flags</span></span>           | <span data-ttu-id="652c5-312">0x00000013</span><span class="sxs-lookup"><span data-stu-id="652c5-312">0x00000013</span></span>                      |
| <span data-ttu-id="652c5-313">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="652c5-313">Classes used in</span></span>        | [<span data-ttu-id="652c5-314">**Início**</span><span class="sxs-lookup"><span data-stu-id="652c5-314">**Top**</span></span>](c-top.md)<br/> |



 

 





