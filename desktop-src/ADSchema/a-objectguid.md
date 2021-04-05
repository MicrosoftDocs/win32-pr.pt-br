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
# <a name="object-guid-attribute"></a><span data-ttu-id="4a504-105">Object-Guid atributo</span><span class="sxs-lookup"><span data-stu-id="4a504-105">Object-Guid attribute</span></span>

<span data-ttu-id="4a504-106">O identificador exclusivo de um objeto.</span><span class="sxs-lookup"><span data-stu-id="4a504-106">The unique identifier for an object.</span></span>



| <span data-ttu-id="4a504-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="4a504-107">Entry</span></span> | <span data-ttu-id="4a504-108">Valor</span><span class="sxs-lookup"><span data-stu-id="4a504-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------|
| <span data-ttu-id="4a504-109">CN</span><span class="sxs-lookup"><span data-stu-id="4a504-109">CN</span></span>                | <span data-ttu-id="4a504-110">Object-Guid</span><span class="sxs-lookup"><span data-stu-id="4a504-110">Object-Guid</span></span>                                                         |
| <span data-ttu-id="4a504-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4a504-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4a504-112">objectGUID</span><span class="sxs-lookup"><span data-stu-id="4a504-112">objectGUID</span></span>                                                          |
| <span data-ttu-id="4a504-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="4a504-113">Size</span></span>              | <span data-ttu-id="4a504-114">16 bytes</span><span class="sxs-lookup"><span data-stu-id="4a504-114">16 bytes</span></span>                                                            |
| <span data-ttu-id="4a504-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="4a504-115">Update Privilege</span></span>  | <span data-ttu-id="4a504-116">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="4a504-116">This value is set by the system.</span></span>                                    |
| <span data-ttu-id="4a504-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="4a504-117">Update Frequency</span></span>  | <span data-ttu-id="4a504-118">Esse valor é definido quando o objeto é criado e não pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="4a504-118">This value is set when the object is created and cannot be changed.</span></span> |
| <span data-ttu-id="4a504-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4a504-119">Attribute-Id</span></span>      | <span data-ttu-id="4a504-120">1.2.840.113556.1.4.2</span><span class="sxs-lookup"><span data-stu-id="4a504-120">1.2.840.113556.1.4.2</span></span>                                                |
| <span data-ttu-id="4a504-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4a504-121">System-Id-Guid</span></span>    | <span data-ttu-id="4a504-122">bf9679e7-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="4a504-122">bf9679e7-0de6-11d0-a285-00aa003049e2</span></span>                                |
| <span data-ttu-id="4a504-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a504-123">Syntax</span></span>            | [<span data-ttu-id="4a504-124">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="4a504-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)               |



## <a name="implementations"></a><span data-ttu-id="4a504-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="4a504-125">Implementations</span></span>

-   [<span data-ttu-id="4a504-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4a504-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4a504-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4a504-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4a504-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="4a504-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="4a504-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4a504-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4a504-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4a504-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4a504-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4a504-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4a504-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4a504-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4a504-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4a504-133">Windows 2000 Server</span></span>



| <span data-ttu-id="4a504-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="4a504-134">Entry</span></span> | <span data-ttu-id="4a504-135">Valor</span><span class="sxs-lookup"><span data-stu-id="4a504-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4a504-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="4a504-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="4a504-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a504-137">MAPI-Id</span></span>                | <span data-ttu-id="4a504-138">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="4a504-138">0x8C6D</span></span>                          |
| <span data-ttu-id="4a504-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a504-139">System-Only</span></span>            | <span data-ttu-id="4a504-140">True</span><span class="sxs-lookup"><span data-stu-id="4a504-140">True</span></span>                            |
| <span data-ttu-id="4a504-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4a504-141">Is-Single-Valued</span></span>       | <span data-ttu-id="4a504-142">True</span><span class="sxs-lookup"><span data-stu-id="4a504-142">True</span></span>                            |
| <span data-ttu-id="4a504-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="4a504-143">Is Indexed</span></span>             | <span data-ttu-id="4a504-144">True</span><span class="sxs-lookup"><span data-stu-id="4a504-144">True</span></span>                            |
| <span data-ttu-id="4a504-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4a504-145">In Global Catalog</span></span>      | <span data-ttu-id="4a504-146">True</span><span class="sxs-lookup"><span data-stu-id="4a504-146">True</span></span>                            |
| <span data-ttu-id="4a504-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4a504-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a504-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4a504-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4a504-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a504-149">Range-Lower</span></span>            | <span data-ttu-id="4a504-150">16</span><span class="sxs-lookup"><span data-stu-id="4a504-150">16</span></span>                              |
| <span data-ttu-id="4a504-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a504-151">Range-Upper</span></span>            | <span data-ttu-id="4a504-152">16</span><span class="sxs-lookup"><span data-stu-id="4a504-152">16</span></span>                              |
| <span data-ttu-id="4a504-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a504-153">Search-Flags</span></span>           | <span data-ttu-id="4a504-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="4a504-154">0x00000009</span></span>                      |
| <span data-ttu-id="4a504-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a504-155">System-Flags</span></span>           | <span data-ttu-id="4a504-156">0x00000013</span><span class="sxs-lookup"><span data-stu-id="4a504-156">0x00000013</span></span>                      |
| <span data-ttu-id="4a504-157">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4a504-157">Classes used in</span></span>        | [<span data-ttu-id="4a504-158">**Início**</span><span class="sxs-lookup"><span data-stu-id="4a504-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4a504-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4a504-159">Windows Server 2003</span></span>



| <span data-ttu-id="4a504-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="4a504-160">Entry</span></span> | <span data-ttu-id="4a504-161">Valor</span><span class="sxs-lookup"><span data-stu-id="4a504-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4a504-162">ID do link</span><span class="sxs-lookup"><span data-stu-id="4a504-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="4a504-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a504-163">MAPI-Id</span></span>                | <span data-ttu-id="4a504-164">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="4a504-164">0x8C6D</span></span>                          |
| <span data-ttu-id="4a504-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a504-165">System-Only</span></span>            | <span data-ttu-id="4a504-166">True</span><span class="sxs-lookup"><span data-stu-id="4a504-166">True</span></span>                            |
| <span data-ttu-id="4a504-167">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4a504-167">Is-Single-Valued</span></span>       | <span data-ttu-id="4a504-168">True</span><span class="sxs-lookup"><span data-stu-id="4a504-168">True</span></span>                            |
| <span data-ttu-id="4a504-169">É indexado</span><span class="sxs-lookup"><span data-stu-id="4a504-169">Is Indexed</span></span>             | <span data-ttu-id="4a504-170">True</span><span class="sxs-lookup"><span data-stu-id="4a504-170">True</span></span>                            |
| <span data-ttu-id="4a504-171">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4a504-171">In Global Catalog</span></span>      | <span data-ttu-id="4a504-172">True</span><span class="sxs-lookup"><span data-stu-id="4a504-172">True</span></span>                            |
| <span data-ttu-id="4a504-173">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4a504-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a504-174">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4a504-174">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4a504-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a504-175">Range-Lower</span></span>            | <span data-ttu-id="4a504-176">16</span><span class="sxs-lookup"><span data-stu-id="4a504-176">16</span></span>                              |
| <span data-ttu-id="4a504-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a504-177">Range-Upper</span></span>            | <span data-ttu-id="4a504-178">16</span><span class="sxs-lookup"><span data-stu-id="4a504-178">16</span></span>                              |
| <span data-ttu-id="4a504-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a504-179">Search-Flags</span></span>           | <span data-ttu-id="4a504-180">0x00000009</span><span class="sxs-lookup"><span data-stu-id="4a504-180">0x00000009</span></span>                      |
| <span data-ttu-id="4a504-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a504-181">System-Flags</span></span>           | <span data-ttu-id="4a504-182">0x00000013</span><span class="sxs-lookup"><span data-stu-id="4a504-182">0x00000013</span></span>                      |
| <span data-ttu-id="4a504-183">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4a504-183">Classes used in</span></span>        | [<span data-ttu-id="4a504-184">**Início**</span><span class="sxs-lookup"><span data-stu-id="4a504-184">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="4a504-185">ADAM</span><span class="sxs-lookup"><span data-stu-id="4a504-185">ADAM</span></span>



| <span data-ttu-id="4a504-186">Entrada</span><span class="sxs-lookup"><span data-stu-id="4a504-186">Entry</span></span> | <span data-ttu-id="4a504-187">Valor</span><span class="sxs-lookup"><span data-stu-id="4a504-187">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4a504-188">ID do link</span><span class="sxs-lookup"><span data-stu-id="4a504-188">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="4a504-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a504-189">MAPI-Id</span></span>                | <span data-ttu-id="4a504-190">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="4a504-190">0x8C6D</span></span>                          |
| <span data-ttu-id="4a504-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a504-191">System-Only</span></span>            | <span data-ttu-id="4a504-192">True</span><span class="sxs-lookup"><span data-stu-id="4a504-192">True</span></span>                            |
| <span data-ttu-id="4a504-193">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4a504-193">Is-Single-Valued</span></span>       | <span data-ttu-id="4a504-194">True</span><span class="sxs-lookup"><span data-stu-id="4a504-194">True</span></span>                            |
| <span data-ttu-id="4a504-195">É indexado</span><span class="sxs-lookup"><span data-stu-id="4a504-195">Is Indexed</span></span>             | <span data-ttu-id="4a504-196">True</span><span class="sxs-lookup"><span data-stu-id="4a504-196">True</span></span>                            |
| <span data-ttu-id="4a504-197">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4a504-197">In Global Catalog</span></span>      | <span data-ttu-id="4a504-198">True</span><span class="sxs-lookup"><span data-stu-id="4a504-198">True</span></span>                            |
| <span data-ttu-id="4a504-199">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4a504-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a504-200">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4a504-200">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4a504-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a504-201">Range-Lower</span></span>            | <span data-ttu-id="4a504-202">16</span><span class="sxs-lookup"><span data-stu-id="4a504-202">16</span></span>                              |
| <span data-ttu-id="4a504-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a504-203">Range-Upper</span></span>            | <span data-ttu-id="4a504-204">16</span><span class="sxs-lookup"><span data-stu-id="4a504-204">16</span></span>                              |
| <span data-ttu-id="4a504-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a504-205">Search-Flags</span></span>           | <span data-ttu-id="4a504-206">0x00000009</span><span class="sxs-lookup"><span data-stu-id="4a504-206">0x00000009</span></span>                      |
| <span data-ttu-id="4a504-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a504-207">System-Flags</span></span>           | <span data-ttu-id="4a504-208">0x00000013</span><span class="sxs-lookup"><span data-stu-id="4a504-208">0x00000013</span></span>                      |
| <span data-ttu-id="4a504-209">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4a504-209">Classes used in</span></span>        | [<span data-ttu-id="4a504-210">**Início**</span><span class="sxs-lookup"><span data-stu-id="4a504-210">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4a504-211">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4a504-211">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4a504-212">Entrada</span><span class="sxs-lookup"><span data-stu-id="4a504-212">Entry</span></span> | <span data-ttu-id="4a504-213">Valor</span><span class="sxs-lookup"><span data-stu-id="4a504-213">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4a504-214">ID do link</span><span class="sxs-lookup"><span data-stu-id="4a504-214">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="4a504-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a504-215">MAPI-Id</span></span>                | <span data-ttu-id="4a504-216">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="4a504-216">0x8C6D</span></span>                          |
| <span data-ttu-id="4a504-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a504-217">System-Only</span></span>            | <span data-ttu-id="4a504-218">True</span><span class="sxs-lookup"><span data-stu-id="4a504-218">True</span></span>                            |
| <span data-ttu-id="4a504-219">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4a504-219">Is-Single-Valued</span></span>       | <span data-ttu-id="4a504-220">True</span><span class="sxs-lookup"><span data-stu-id="4a504-220">True</span></span>                            |
| <span data-ttu-id="4a504-221">É indexado</span><span class="sxs-lookup"><span data-stu-id="4a504-221">Is Indexed</span></span>             | <span data-ttu-id="4a504-222">True</span><span class="sxs-lookup"><span data-stu-id="4a504-222">True</span></span>                            |
| <span data-ttu-id="4a504-223">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4a504-223">In Global Catalog</span></span>      | <span data-ttu-id="4a504-224">True</span><span class="sxs-lookup"><span data-stu-id="4a504-224">True</span></span>                            |
| <span data-ttu-id="4a504-225">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4a504-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a504-226">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4a504-226">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4a504-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a504-227">Range-Lower</span></span>            | <span data-ttu-id="4a504-228">16</span><span class="sxs-lookup"><span data-stu-id="4a504-228">16</span></span>                              |
| <span data-ttu-id="4a504-229">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a504-229">Range-Upper</span></span>            | <span data-ttu-id="4a504-230">16</span><span class="sxs-lookup"><span data-stu-id="4a504-230">16</span></span>                              |
| <span data-ttu-id="4a504-231">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a504-231">Search-Flags</span></span>           | <span data-ttu-id="4a504-232">0x00000009</span><span class="sxs-lookup"><span data-stu-id="4a504-232">0x00000009</span></span>                      |
| <span data-ttu-id="4a504-233">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a504-233">System-Flags</span></span>           | <span data-ttu-id="4a504-234">0x00000013</span><span class="sxs-lookup"><span data-stu-id="4a504-234">0x00000013</span></span>                      |
| <span data-ttu-id="4a504-235">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4a504-235">Classes used in</span></span>        | [<span data-ttu-id="4a504-236">**Início**</span><span class="sxs-lookup"><span data-stu-id="4a504-236">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4a504-237">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4a504-237">Windows Server 2008</span></span>



| <span data-ttu-id="4a504-238">Entrada</span><span class="sxs-lookup"><span data-stu-id="4a504-238">Entry</span></span> | <span data-ttu-id="4a504-239">Valor</span><span class="sxs-lookup"><span data-stu-id="4a504-239">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4a504-240">ID do link</span><span class="sxs-lookup"><span data-stu-id="4a504-240">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="4a504-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a504-241">MAPI-Id</span></span>                | <span data-ttu-id="4a504-242">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="4a504-242">0x8C6D</span></span>                          |
| <span data-ttu-id="4a504-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a504-243">System-Only</span></span>            | <span data-ttu-id="4a504-244">True</span><span class="sxs-lookup"><span data-stu-id="4a504-244">True</span></span>                            |
| <span data-ttu-id="4a504-245">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4a504-245">Is-Single-Valued</span></span>       | <span data-ttu-id="4a504-246">True</span><span class="sxs-lookup"><span data-stu-id="4a504-246">True</span></span>                            |
| <span data-ttu-id="4a504-247">É indexado</span><span class="sxs-lookup"><span data-stu-id="4a504-247">Is Indexed</span></span>             | <span data-ttu-id="4a504-248">True</span><span class="sxs-lookup"><span data-stu-id="4a504-248">True</span></span>                            |
| <span data-ttu-id="4a504-249">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4a504-249">In Global Catalog</span></span>      | <span data-ttu-id="4a504-250">True</span><span class="sxs-lookup"><span data-stu-id="4a504-250">True</span></span>                            |
| <span data-ttu-id="4a504-251">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4a504-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a504-252">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4a504-252">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4a504-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a504-253">Range-Lower</span></span>            | <span data-ttu-id="4a504-254">16</span><span class="sxs-lookup"><span data-stu-id="4a504-254">16</span></span>                              |
| <span data-ttu-id="4a504-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a504-255">Range-Upper</span></span>            | <span data-ttu-id="4a504-256">16</span><span class="sxs-lookup"><span data-stu-id="4a504-256">16</span></span>                              |
| <span data-ttu-id="4a504-257">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a504-257">Search-Flags</span></span>           | <span data-ttu-id="4a504-258">0x00000009</span><span class="sxs-lookup"><span data-stu-id="4a504-258">0x00000009</span></span>                      |
| <span data-ttu-id="4a504-259">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a504-259">System-Flags</span></span>           | <span data-ttu-id="4a504-260">0x00000013</span><span class="sxs-lookup"><span data-stu-id="4a504-260">0x00000013</span></span>                      |
| <span data-ttu-id="4a504-261">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4a504-261">Classes used in</span></span>        | [<span data-ttu-id="4a504-262">**Início**</span><span class="sxs-lookup"><span data-stu-id="4a504-262">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4a504-263">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4a504-263">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4a504-264">Entrada</span><span class="sxs-lookup"><span data-stu-id="4a504-264">Entry</span></span> | <span data-ttu-id="4a504-265">Valor</span><span class="sxs-lookup"><span data-stu-id="4a504-265">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4a504-266">ID do link</span><span class="sxs-lookup"><span data-stu-id="4a504-266">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="4a504-267">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a504-267">MAPI-Id</span></span>                | <span data-ttu-id="4a504-268">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="4a504-268">0x8C6D</span></span>                          |
| <span data-ttu-id="4a504-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a504-269">System-Only</span></span>            | <span data-ttu-id="4a504-270">True</span><span class="sxs-lookup"><span data-stu-id="4a504-270">True</span></span>                            |
| <span data-ttu-id="4a504-271">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4a504-271">Is-Single-Valued</span></span>       | <span data-ttu-id="4a504-272">True</span><span class="sxs-lookup"><span data-stu-id="4a504-272">True</span></span>                            |
| <span data-ttu-id="4a504-273">É indexado</span><span class="sxs-lookup"><span data-stu-id="4a504-273">Is Indexed</span></span>             | <span data-ttu-id="4a504-274">True</span><span class="sxs-lookup"><span data-stu-id="4a504-274">True</span></span>                            |
| <span data-ttu-id="4a504-275">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4a504-275">In Global Catalog</span></span>      | <span data-ttu-id="4a504-276">True</span><span class="sxs-lookup"><span data-stu-id="4a504-276">True</span></span>                            |
| <span data-ttu-id="4a504-277">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4a504-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a504-278">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4a504-278">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4a504-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a504-279">Range-Lower</span></span>            | <span data-ttu-id="4a504-280">16</span><span class="sxs-lookup"><span data-stu-id="4a504-280">16</span></span>                              |
| <span data-ttu-id="4a504-281">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a504-281">Range-Upper</span></span>            | <span data-ttu-id="4a504-282">16</span><span class="sxs-lookup"><span data-stu-id="4a504-282">16</span></span>                              |
| <span data-ttu-id="4a504-283">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a504-283">Search-Flags</span></span>           | <span data-ttu-id="4a504-284">0x00000009</span><span class="sxs-lookup"><span data-stu-id="4a504-284">0x00000009</span></span>                      |
| <span data-ttu-id="4a504-285">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a504-285">System-Flags</span></span>           | <span data-ttu-id="4a504-286">0x00000013</span><span class="sxs-lookup"><span data-stu-id="4a504-286">0x00000013</span></span>                      |
| <span data-ttu-id="4a504-287">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4a504-287">Classes used in</span></span>        | [<span data-ttu-id="4a504-288">**Início**</span><span class="sxs-lookup"><span data-stu-id="4a504-288">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4a504-289">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4a504-289">Windows Server 2012</span></span>



| <span data-ttu-id="4a504-290">Entrada</span><span class="sxs-lookup"><span data-stu-id="4a504-290">Entry</span></span> | <span data-ttu-id="4a504-291">Valor</span><span class="sxs-lookup"><span data-stu-id="4a504-291">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="4a504-292">ID do link</span><span class="sxs-lookup"><span data-stu-id="4a504-292">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="4a504-293">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a504-293">MAPI-Id</span></span>                | <span data-ttu-id="4a504-294">0x8C6D</span><span class="sxs-lookup"><span data-stu-id="4a504-294">0x8C6D</span></span>                          |
| <span data-ttu-id="4a504-295">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a504-295">System-Only</span></span>            | <span data-ttu-id="4a504-296">True</span><span class="sxs-lookup"><span data-stu-id="4a504-296">True</span></span>                            |
| <span data-ttu-id="4a504-297">É de valor único</span><span class="sxs-lookup"><span data-stu-id="4a504-297">Is-Single-Valued</span></span>       | <span data-ttu-id="4a504-298">True</span><span class="sxs-lookup"><span data-stu-id="4a504-298">True</span></span>                            |
| <span data-ttu-id="4a504-299">É indexado</span><span class="sxs-lookup"><span data-stu-id="4a504-299">Is Indexed</span></span>             | <span data-ttu-id="4a504-300">True</span><span class="sxs-lookup"><span data-stu-id="4a504-300">True</span></span>                            |
| <span data-ttu-id="4a504-301">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="4a504-301">In Global Catalog</span></span>      | <span data-ttu-id="4a504-302">True</span><span class="sxs-lookup"><span data-stu-id="4a504-302">True</span></span>                            |
| <span data-ttu-id="4a504-303">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="4a504-303">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a504-304">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="4a504-304">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="4a504-305">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a504-305">Range-Lower</span></span>            | <span data-ttu-id="4a504-306">16</span><span class="sxs-lookup"><span data-stu-id="4a504-306">16</span></span>                              |
| <span data-ttu-id="4a504-307">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a504-307">Range-Upper</span></span>            | <span data-ttu-id="4a504-308">16</span><span class="sxs-lookup"><span data-stu-id="4a504-308">16</span></span>                              |
| <span data-ttu-id="4a504-309">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a504-309">Search-Flags</span></span>           | <span data-ttu-id="4a504-310">0x00000009</span><span class="sxs-lookup"><span data-stu-id="4a504-310">0x00000009</span></span>                      |
| <span data-ttu-id="4a504-311">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a504-311">System-Flags</span></span>           | <span data-ttu-id="4a504-312">0x00000013</span><span class="sxs-lookup"><span data-stu-id="4a504-312">0x00000013</span></span>                      |
| <span data-ttu-id="4a504-313">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="4a504-313">Classes used in</span></span>        | [<span data-ttu-id="4a504-314">**Início**</span><span class="sxs-lookup"><span data-stu-id="4a504-314">**Top**</span></span>](c-top.md)<br/> |



 

 





