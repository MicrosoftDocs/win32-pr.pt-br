---
title: Atributo pai-GUID
description: Este é um atributo construído, inventado para dar suporte ao controle DirSync. Esse atributo contém o objectGUID do pai de um objeto ao replicar a criação, renomeação ou movimentação de um objeto.
ms.assetid: caf2491b-c0bf-4ea1-80ec-d44cf9307551
ms.tgt_platform: multiple
keywords:
- Atributo pai-GUID AD Schema
- Esquema de AD do atributo parentGUID
topic_type:
- apiref
api_name:
- Parent-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38b01faf958f4add9c7788d630321d7c225f5026
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825298"
---
# <a name="parent-guid-attribute"></a><span data-ttu-id="758e7-106">Atributo pai-GUID</span><span class="sxs-lookup"><span data-stu-id="758e7-106">Parent-GUID attribute</span></span>

<span data-ttu-id="758e7-107">Este é um atributo construído, inventado para dar suporte ao controle DirSync.</span><span class="sxs-lookup"><span data-stu-id="758e7-107">This is a constructed attribute, invented to support the DirSync control.</span></span> <span data-ttu-id="758e7-108">Esse atributo contém o objectGUID do pai de um objeto ao replicar a criação, renomeação ou movimentação de um objeto.</span><span class="sxs-lookup"><span data-stu-id="758e7-108">This attribute holds the objectGuid of an object's parent when replicating an object's creation, rename, or move.</span></span>



| <span data-ttu-id="758e7-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="758e7-109">Entry</span></span> | <span data-ttu-id="758e7-110">Valor</span><span class="sxs-lookup"><span data-stu-id="758e7-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="758e7-111">CN</span><span class="sxs-lookup"><span data-stu-id="758e7-111">CN</span></span>                | <span data-ttu-id="758e7-112">GUID-pai</span><span class="sxs-lookup"><span data-stu-id="758e7-112">Parent-GUID</span></span>                                           |
| <span data-ttu-id="758e7-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="758e7-113">Ldap-Display-Name</span></span> | <span data-ttu-id="758e7-114">parentGUID</span><span class="sxs-lookup"><span data-stu-id="758e7-114">parentGUID</span></span>                                            |
| <span data-ttu-id="758e7-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="758e7-115">Size</span></span>              | <span data-ttu-id="758e7-116">16 bytes</span><span class="sxs-lookup"><span data-stu-id="758e7-116">16 bytes</span></span>                                              |
| <span data-ttu-id="758e7-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="758e7-117">Update Privilege</span></span>  | <span data-ttu-id="758e7-118">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="758e7-118">This value is set by the system.</span></span>                      |
| <span data-ttu-id="758e7-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="758e7-119">Update Frequency</span></span>  | <span data-ttu-id="758e7-120">Durante a replicação</span><span class="sxs-lookup"><span data-stu-id="758e7-120">During replication</span></span>                                    |
| <span data-ttu-id="758e7-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="758e7-121">Attribute-Id</span></span>      | <span data-ttu-id="758e7-122">1.2.840.113556.1.4.1224</span><span class="sxs-lookup"><span data-stu-id="758e7-122">1.2.840.113556.1.4.1224</span></span>                               |
| <span data-ttu-id="758e7-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="758e7-123">System-Id-Guid</span></span>    | <span data-ttu-id="758e7-124">2df90d74-009f-11d2-aa4c-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="758e7-124">2df90d74-009f-11d2-aa4c-00c04fd7d83a</span></span>                  |
| <span data-ttu-id="758e7-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="758e7-125">Syntax</span></span>            | [<span data-ttu-id="758e7-126">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="758e7-126">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="758e7-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="758e7-127">Implementations</span></span>

-   [<span data-ttu-id="758e7-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="758e7-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="758e7-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="758e7-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="758e7-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="758e7-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="758e7-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="758e7-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="758e7-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="758e7-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="758e7-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="758e7-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="758e7-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="758e7-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="758e7-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="758e7-135">Windows 2000 Server</span></span>



| <span data-ttu-id="758e7-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="758e7-136">Entry</span></span> | <span data-ttu-id="758e7-137">Valor</span><span class="sxs-lookup"><span data-stu-id="758e7-137">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="758e7-138">ID do link</span><span class="sxs-lookup"><span data-stu-id="758e7-138">Link-Id</span></span>                | \-           |
| <span data-ttu-id="758e7-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="758e7-139">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="758e7-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="758e7-140">System-Only</span></span>            | <span data-ttu-id="758e7-141">True</span><span class="sxs-lookup"><span data-stu-id="758e7-141">True</span></span>         |
| <span data-ttu-id="758e7-142">É de valor único</span><span class="sxs-lookup"><span data-stu-id="758e7-142">Is-Single-Valued</span></span>       | <span data-ttu-id="758e7-143">True</span><span class="sxs-lookup"><span data-stu-id="758e7-143">True</span></span>         |
| <span data-ttu-id="758e7-144">É indexado</span><span class="sxs-lookup"><span data-stu-id="758e7-144">Is Indexed</span></span>             | <span data-ttu-id="758e7-145">Falso</span><span class="sxs-lookup"><span data-stu-id="758e7-145">False</span></span>        |
| <span data-ttu-id="758e7-146">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="758e7-146">In Global Catalog</span></span>      | <span data-ttu-id="758e7-147">Falso</span><span class="sxs-lookup"><span data-stu-id="758e7-147">False</span></span>        |
| <span data-ttu-id="758e7-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="758e7-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="758e7-149">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="758e7-149">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="758e7-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="758e7-150">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="758e7-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="758e7-151">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="758e7-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="758e7-152">Search-Flags</span></span>           | <span data-ttu-id="758e7-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="758e7-153">0x00000000</span></span>   |
| <span data-ttu-id="758e7-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="758e7-154">System-Flags</span></span>           | <span data-ttu-id="758e7-155">0x08000014</span><span class="sxs-lookup"><span data-stu-id="758e7-155">0x08000014</span></span>   |
| <span data-ttu-id="758e7-156">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="758e7-156">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003"></a><span data-ttu-id="758e7-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="758e7-157">Windows Server 2003</span></span>



| <span data-ttu-id="758e7-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="758e7-158">Entry</span></span> | <span data-ttu-id="758e7-159">Valor</span><span class="sxs-lookup"><span data-stu-id="758e7-159">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="758e7-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="758e7-160">Link-Id</span></span>                | \-           |
| <span data-ttu-id="758e7-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="758e7-161">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="758e7-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="758e7-162">System-Only</span></span>            | <span data-ttu-id="758e7-163">True</span><span class="sxs-lookup"><span data-stu-id="758e7-163">True</span></span>         |
| <span data-ttu-id="758e7-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="758e7-164">Is-Single-Valued</span></span>       | <span data-ttu-id="758e7-165">True</span><span class="sxs-lookup"><span data-stu-id="758e7-165">True</span></span>         |
| <span data-ttu-id="758e7-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="758e7-166">Is Indexed</span></span>             | <span data-ttu-id="758e7-167">Falso</span><span class="sxs-lookup"><span data-stu-id="758e7-167">False</span></span>        |
| <span data-ttu-id="758e7-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="758e7-168">In Global Catalog</span></span>      | <span data-ttu-id="758e7-169">Falso</span><span class="sxs-lookup"><span data-stu-id="758e7-169">False</span></span>        |
| <span data-ttu-id="758e7-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="758e7-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="758e7-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="758e7-171">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="758e7-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="758e7-172">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="758e7-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="758e7-173">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="758e7-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="758e7-174">Search-Flags</span></span>           | <span data-ttu-id="758e7-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="758e7-175">0x00000000</span></span>   |
| <span data-ttu-id="758e7-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="758e7-176">System-Flags</span></span>           | <span data-ttu-id="758e7-177">0x08000014</span><span class="sxs-lookup"><span data-stu-id="758e7-177">0x08000014</span></span>   |
| <span data-ttu-id="758e7-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="758e7-178">Classes used in</span></span>        | \-           |



## <a name="adam"></a><span data-ttu-id="758e7-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="758e7-179">ADAM</span></span>



| <span data-ttu-id="758e7-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="758e7-180">Entry</span></span> | <span data-ttu-id="758e7-181">Valor</span><span class="sxs-lookup"><span data-stu-id="758e7-181">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="758e7-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="758e7-182">Link-Id</span></span>                | \-           |
| <span data-ttu-id="758e7-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="758e7-183">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="758e7-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="758e7-184">System-Only</span></span>            | <span data-ttu-id="758e7-185">True</span><span class="sxs-lookup"><span data-stu-id="758e7-185">True</span></span>         |
| <span data-ttu-id="758e7-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="758e7-186">Is-Single-Valued</span></span>       | <span data-ttu-id="758e7-187">True</span><span class="sxs-lookup"><span data-stu-id="758e7-187">True</span></span>         |
| <span data-ttu-id="758e7-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="758e7-188">Is Indexed</span></span>             | <span data-ttu-id="758e7-189">Falso</span><span class="sxs-lookup"><span data-stu-id="758e7-189">False</span></span>        |
| <span data-ttu-id="758e7-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="758e7-190">In Global Catalog</span></span>      | <span data-ttu-id="758e7-191">Falso</span><span class="sxs-lookup"><span data-stu-id="758e7-191">False</span></span>        |
| <span data-ttu-id="758e7-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="758e7-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="758e7-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="758e7-193">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="758e7-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="758e7-194">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="758e7-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="758e7-195">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="758e7-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="758e7-196">Search-Flags</span></span>           | <span data-ttu-id="758e7-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="758e7-197">0x00000000</span></span>   |
| <span data-ttu-id="758e7-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="758e7-198">System-Flags</span></span>           | <span data-ttu-id="758e7-199">0x08000014</span><span class="sxs-lookup"><span data-stu-id="758e7-199">0x08000014</span></span>   |
| <span data-ttu-id="758e7-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="758e7-200">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="758e7-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="758e7-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="758e7-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="758e7-202">Entry</span></span> | <span data-ttu-id="758e7-203">Valor</span><span class="sxs-lookup"><span data-stu-id="758e7-203">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="758e7-204">ID do link</span><span class="sxs-lookup"><span data-stu-id="758e7-204">Link-Id</span></span>                | \-           |
| <span data-ttu-id="758e7-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="758e7-205">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="758e7-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="758e7-206">System-Only</span></span>            | <span data-ttu-id="758e7-207">True</span><span class="sxs-lookup"><span data-stu-id="758e7-207">True</span></span>         |
| <span data-ttu-id="758e7-208">É de valor único</span><span class="sxs-lookup"><span data-stu-id="758e7-208">Is-Single-Valued</span></span>       | <span data-ttu-id="758e7-209">True</span><span class="sxs-lookup"><span data-stu-id="758e7-209">True</span></span>         |
| <span data-ttu-id="758e7-210">É indexado</span><span class="sxs-lookup"><span data-stu-id="758e7-210">Is Indexed</span></span>             | <span data-ttu-id="758e7-211">Falso</span><span class="sxs-lookup"><span data-stu-id="758e7-211">False</span></span>        |
| <span data-ttu-id="758e7-212">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="758e7-212">In Global Catalog</span></span>      | <span data-ttu-id="758e7-213">Falso</span><span class="sxs-lookup"><span data-stu-id="758e7-213">False</span></span>        |
| <span data-ttu-id="758e7-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="758e7-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="758e7-215">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="758e7-215">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="758e7-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="758e7-216">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="758e7-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="758e7-217">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="758e7-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="758e7-218">Search-Flags</span></span>           | <span data-ttu-id="758e7-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="758e7-219">0x00000000</span></span>   |
| <span data-ttu-id="758e7-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="758e7-220">System-Flags</span></span>           | <span data-ttu-id="758e7-221">0x08000014</span><span class="sxs-lookup"><span data-stu-id="758e7-221">0x08000014</span></span>   |
| <span data-ttu-id="758e7-222">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="758e7-222">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="758e7-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="758e7-223">Windows Server 2008</span></span>



| <span data-ttu-id="758e7-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="758e7-224">Entry</span></span> | <span data-ttu-id="758e7-225">Valor</span><span class="sxs-lookup"><span data-stu-id="758e7-225">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="758e7-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="758e7-226">Link-Id</span></span>                | \-           |
| <span data-ttu-id="758e7-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="758e7-227">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="758e7-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="758e7-228">System-Only</span></span>            | <span data-ttu-id="758e7-229">True</span><span class="sxs-lookup"><span data-stu-id="758e7-229">True</span></span>         |
| <span data-ttu-id="758e7-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="758e7-230">Is-Single-Valued</span></span>       | <span data-ttu-id="758e7-231">True</span><span class="sxs-lookup"><span data-stu-id="758e7-231">True</span></span>         |
| <span data-ttu-id="758e7-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="758e7-232">Is Indexed</span></span>             | <span data-ttu-id="758e7-233">Falso</span><span class="sxs-lookup"><span data-stu-id="758e7-233">False</span></span>        |
| <span data-ttu-id="758e7-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="758e7-234">In Global Catalog</span></span>      | <span data-ttu-id="758e7-235">Falso</span><span class="sxs-lookup"><span data-stu-id="758e7-235">False</span></span>        |
| <span data-ttu-id="758e7-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="758e7-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="758e7-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="758e7-237">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="758e7-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="758e7-238">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="758e7-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="758e7-239">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="758e7-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="758e7-240">Search-Flags</span></span>           | <span data-ttu-id="758e7-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="758e7-241">0x00000000</span></span>   |
| <span data-ttu-id="758e7-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="758e7-242">System-Flags</span></span>           | <span data-ttu-id="758e7-243">0x08000014</span><span class="sxs-lookup"><span data-stu-id="758e7-243">0x08000014</span></span>   |
| <span data-ttu-id="758e7-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="758e7-244">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="758e7-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="758e7-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="758e7-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="758e7-246">Entry</span></span> | <span data-ttu-id="758e7-247">Valor</span><span class="sxs-lookup"><span data-stu-id="758e7-247">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="758e7-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="758e7-248">Link-Id</span></span>                | \-           |
| <span data-ttu-id="758e7-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="758e7-249">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="758e7-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="758e7-250">System-Only</span></span>            | <span data-ttu-id="758e7-251">True</span><span class="sxs-lookup"><span data-stu-id="758e7-251">True</span></span>         |
| <span data-ttu-id="758e7-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="758e7-252">Is-Single-Valued</span></span>       | <span data-ttu-id="758e7-253">True</span><span class="sxs-lookup"><span data-stu-id="758e7-253">True</span></span>         |
| <span data-ttu-id="758e7-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="758e7-254">Is Indexed</span></span>             | <span data-ttu-id="758e7-255">Falso</span><span class="sxs-lookup"><span data-stu-id="758e7-255">False</span></span>        |
| <span data-ttu-id="758e7-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="758e7-256">In Global Catalog</span></span>      | <span data-ttu-id="758e7-257">Falso</span><span class="sxs-lookup"><span data-stu-id="758e7-257">False</span></span>        |
| <span data-ttu-id="758e7-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="758e7-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="758e7-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="758e7-259">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="758e7-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="758e7-260">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="758e7-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="758e7-261">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="758e7-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="758e7-262">Search-Flags</span></span>           | <span data-ttu-id="758e7-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="758e7-263">0x00000000</span></span>   |
| <span data-ttu-id="758e7-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="758e7-264">System-Flags</span></span>           | <span data-ttu-id="758e7-265">0x08000014</span><span class="sxs-lookup"><span data-stu-id="758e7-265">0x08000014</span></span>   |
| <span data-ttu-id="758e7-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="758e7-266">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="758e7-267">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="758e7-267">Windows Server 2012</span></span>



| <span data-ttu-id="758e7-268">Entrada</span><span class="sxs-lookup"><span data-stu-id="758e7-268">Entry</span></span> | <span data-ttu-id="758e7-269">Valor</span><span class="sxs-lookup"><span data-stu-id="758e7-269">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="758e7-270">ID do link</span><span class="sxs-lookup"><span data-stu-id="758e7-270">Link-Id</span></span>                | \-           |
| <span data-ttu-id="758e7-271">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="758e7-271">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="758e7-272">System-Only</span><span class="sxs-lookup"><span data-stu-id="758e7-272">System-Only</span></span>            | <span data-ttu-id="758e7-273">True</span><span class="sxs-lookup"><span data-stu-id="758e7-273">True</span></span>         |
| <span data-ttu-id="758e7-274">É de valor único</span><span class="sxs-lookup"><span data-stu-id="758e7-274">Is-Single-Valued</span></span>       | <span data-ttu-id="758e7-275">True</span><span class="sxs-lookup"><span data-stu-id="758e7-275">True</span></span>         |
| <span data-ttu-id="758e7-276">É indexado</span><span class="sxs-lookup"><span data-stu-id="758e7-276">Is Indexed</span></span>             | <span data-ttu-id="758e7-277">Falso</span><span class="sxs-lookup"><span data-stu-id="758e7-277">False</span></span>        |
| <span data-ttu-id="758e7-278">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="758e7-278">In Global Catalog</span></span>      | <span data-ttu-id="758e7-279">Falso</span><span class="sxs-lookup"><span data-stu-id="758e7-279">False</span></span>        |
| <span data-ttu-id="758e7-280">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="758e7-280">NT-Security-Descriptor</span></span> | <span data-ttu-id="758e7-281">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="758e7-281">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="758e7-282">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="758e7-282">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="758e7-283">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="758e7-283">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="758e7-284">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="758e7-284">Search-Flags</span></span>           | <span data-ttu-id="758e7-285">0x00000000</span><span class="sxs-lookup"><span data-stu-id="758e7-285">0x00000000</span></span>   |
| <span data-ttu-id="758e7-286">System-Flags</span><span class="sxs-lookup"><span data-stu-id="758e7-286">System-Flags</span></span>           | <span data-ttu-id="758e7-287">0x08000014</span><span class="sxs-lookup"><span data-stu-id="758e7-287">0x08000014</span></span>   |
| <span data-ttu-id="758e7-288">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="758e7-288">Classes used in</span></span>        | \-           |



 

 




