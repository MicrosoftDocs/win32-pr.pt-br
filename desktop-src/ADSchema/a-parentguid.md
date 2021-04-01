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
# <a name="parent-guid-attribute"></a><span data-ttu-id="a20ee-106">Atributo pai-GUID</span><span class="sxs-lookup"><span data-stu-id="a20ee-106">Parent-GUID attribute</span></span>

<span data-ttu-id="a20ee-107">Este é um atributo construído, inventado para dar suporte ao controle DirSync.</span><span class="sxs-lookup"><span data-stu-id="a20ee-107">This is a constructed attribute, invented to support the DirSync control.</span></span> <span data-ttu-id="a20ee-108">Esse atributo contém o objectGUID do pai de um objeto ao replicar a criação, renomeação ou movimentação de um objeto.</span><span class="sxs-lookup"><span data-stu-id="a20ee-108">This attribute holds the objectGuid of an object's parent when replicating an object's creation, rename, or move.</span></span>



| <span data-ttu-id="a20ee-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="a20ee-109">Entry</span></span> | <span data-ttu-id="a20ee-110">Valor</span><span class="sxs-lookup"><span data-stu-id="a20ee-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="a20ee-111">CN</span><span class="sxs-lookup"><span data-stu-id="a20ee-111">CN</span></span>                | <span data-ttu-id="a20ee-112">GUID-pai</span><span class="sxs-lookup"><span data-stu-id="a20ee-112">Parent-GUID</span></span>                                           |
| <span data-ttu-id="a20ee-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a20ee-113">Ldap-Display-Name</span></span> | <span data-ttu-id="a20ee-114">parentGUID</span><span class="sxs-lookup"><span data-stu-id="a20ee-114">parentGUID</span></span>                                            |
| <span data-ttu-id="a20ee-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="a20ee-115">Size</span></span>              | <span data-ttu-id="a20ee-116">16 bytes</span><span class="sxs-lookup"><span data-stu-id="a20ee-116">16 bytes</span></span>                                              |
| <span data-ttu-id="a20ee-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="a20ee-117">Update Privilege</span></span>  | <span data-ttu-id="a20ee-118">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="a20ee-118">This value is set by the system.</span></span>                      |
| <span data-ttu-id="a20ee-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="a20ee-119">Update Frequency</span></span>  | <span data-ttu-id="a20ee-120">Durante a replicação</span><span class="sxs-lookup"><span data-stu-id="a20ee-120">During replication</span></span>                                    |
| <span data-ttu-id="a20ee-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a20ee-121">Attribute-Id</span></span>      | <span data-ttu-id="a20ee-122">1.2.840.113556.1.4.1224</span><span class="sxs-lookup"><span data-stu-id="a20ee-122">1.2.840.113556.1.4.1224</span></span>                               |
| <span data-ttu-id="a20ee-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a20ee-123">System-Id-Guid</span></span>    | <span data-ttu-id="a20ee-124">2df90d74-009f-11d2-aa4c-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="a20ee-124">2df90d74-009f-11d2-aa4c-00c04fd7d83a</span></span>                  |
| <span data-ttu-id="a20ee-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="a20ee-125">Syntax</span></span>            | [<span data-ttu-id="a20ee-126">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="a20ee-126">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="a20ee-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="a20ee-127">Implementations</span></span>

-   [<span data-ttu-id="a20ee-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a20ee-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a20ee-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a20ee-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a20ee-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="a20ee-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a20ee-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a20ee-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a20ee-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a20ee-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a20ee-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a20ee-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a20ee-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a20ee-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a20ee-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a20ee-135">Windows 2000 Server</span></span>



| <span data-ttu-id="a20ee-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="a20ee-136">Entry</span></span> | <span data-ttu-id="a20ee-137">Valor</span><span class="sxs-lookup"><span data-stu-id="a20ee-137">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="a20ee-138">ID do link</span><span class="sxs-lookup"><span data-stu-id="a20ee-138">Link-Id</span></span>                | \-           |
| <span data-ttu-id="a20ee-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a20ee-139">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="a20ee-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="a20ee-140">System-Only</span></span>            | <span data-ttu-id="a20ee-141">True</span><span class="sxs-lookup"><span data-stu-id="a20ee-141">True</span></span>         |
| <span data-ttu-id="a20ee-142">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a20ee-142">Is-Single-Valued</span></span>       | <span data-ttu-id="a20ee-143">True</span><span class="sxs-lookup"><span data-stu-id="a20ee-143">True</span></span>         |
| <span data-ttu-id="a20ee-144">É indexado</span><span class="sxs-lookup"><span data-stu-id="a20ee-144">Is Indexed</span></span>             | <span data-ttu-id="a20ee-145">Falso</span><span class="sxs-lookup"><span data-stu-id="a20ee-145">False</span></span>        |
| <span data-ttu-id="a20ee-146">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a20ee-146">In Global Catalog</span></span>      | <span data-ttu-id="a20ee-147">Falso</span><span class="sxs-lookup"><span data-stu-id="a20ee-147">False</span></span>        |
| <span data-ttu-id="a20ee-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a20ee-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="a20ee-149">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a20ee-149">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="a20ee-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a20ee-150">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="a20ee-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a20ee-151">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="a20ee-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a20ee-152">Search-Flags</span></span>           | <span data-ttu-id="a20ee-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a20ee-153">0x00000000</span></span>   |
| <span data-ttu-id="a20ee-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a20ee-154">System-Flags</span></span>           | <span data-ttu-id="a20ee-155">0x08000014</span><span class="sxs-lookup"><span data-stu-id="a20ee-155">0x08000014</span></span>   |
| <span data-ttu-id="a20ee-156">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a20ee-156">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003"></a><span data-ttu-id="a20ee-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a20ee-157">Windows Server 2003</span></span>



| <span data-ttu-id="a20ee-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="a20ee-158">Entry</span></span> | <span data-ttu-id="a20ee-159">Valor</span><span class="sxs-lookup"><span data-stu-id="a20ee-159">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="a20ee-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="a20ee-160">Link-Id</span></span>                | \-           |
| <span data-ttu-id="a20ee-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a20ee-161">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="a20ee-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="a20ee-162">System-Only</span></span>            | <span data-ttu-id="a20ee-163">True</span><span class="sxs-lookup"><span data-stu-id="a20ee-163">True</span></span>         |
| <span data-ttu-id="a20ee-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a20ee-164">Is-Single-Valued</span></span>       | <span data-ttu-id="a20ee-165">True</span><span class="sxs-lookup"><span data-stu-id="a20ee-165">True</span></span>         |
| <span data-ttu-id="a20ee-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="a20ee-166">Is Indexed</span></span>             | <span data-ttu-id="a20ee-167">Falso</span><span class="sxs-lookup"><span data-stu-id="a20ee-167">False</span></span>        |
| <span data-ttu-id="a20ee-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a20ee-168">In Global Catalog</span></span>      | <span data-ttu-id="a20ee-169">Falso</span><span class="sxs-lookup"><span data-stu-id="a20ee-169">False</span></span>        |
| <span data-ttu-id="a20ee-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a20ee-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="a20ee-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a20ee-171">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="a20ee-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a20ee-172">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="a20ee-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a20ee-173">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="a20ee-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a20ee-174">Search-Flags</span></span>           | <span data-ttu-id="a20ee-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a20ee-175">0x00000000</span></span>   |
| <span data-ttu-id="a20ee-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a20ee-176">System-Flags</span></span>           | <span data-ttu-id="a20ee-177">0x08000014</span><span class="sxs-lookup"><span data-stu-id="a20ee-177">0x08000014</span></span>   |
| <span data-ttu-id="a20ee-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a20ee-178">Classes used in</span></span>        | \-           |



## <a name="adam"></a><span data-ttu-id="a20ee-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="a20ee-179">ADAM</span></span>



| <span data-ttu-id="a20ee-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="a20ee-180">Entry</span></span> | <span data-ttu-id="a20ee-181">Valor</span><span class="sxs-lookup"><span data-stu-id="a20ee-181">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="a20ee-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="a20ee-182">Link-Id</span></span>                | \-           |
| <span data-ttu-id="a20ee-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a20ee-183">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="a20ee-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="a20ee-184">System-Only</span></span>            | <span data-ttu-id="a20ee-185">True</span><span class="sxs-lookup"><span data-stu-id="a20ee-185">True</span></span>         |
| <span data-ttu-id="a20ee-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a20ee-186">Is-Single-Valued</span></span>       | <span data-ttu-id="a20ee-187">True</span><span class="sxs-lookup"><span data-stu-id="a20ee-187">True</span></span>         |
| <span data-ttu-id="a20ee-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="a20ee-188">Is Indexed</span></span>             | <span data-ttu-id="a20ee-189">Falso</span><span class="sxs-lookup"><span data-stu-id="a20ee-189">False</span></span>        |
| <span data-ttu-id="a20ee-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a20ee-190">In Global Catalog</span></span>      | <span data-ttu-id="a20ee-191">Falso</span><span class="sxs-lookup"><span data-stu-id="a20ee-191">False</span></span>        |
| <span data-ttu-id="a20ee-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a20ee-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="a20ee-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a20ee-193">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="a20ee-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a20ee-194">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="a20ee-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a20ee-195">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="a20ee-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a20ee-196">Search-Flags</span></span>           | <span data-ttu-id="a20ee-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a20ee-197">0x00000000</span></span>   |
| <span data-ttu-id="a20ee-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a20ee-198">System-Flags</span></span>           | <span data-ttu-id="a20ee-199">0x08000014</span><span class="sxs-lookup"><span data-stu-id="a20ee-199">0x08000014</span></span>   |
| <span data-ttu-id="a20ee-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a20ee-200">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a20ee-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a20ee-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a20ee-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="a20ee-202">Entry</span></span> | <span data-ttu-id="a20ee-203">Valor</span><span class="sxs-lookup"><span data-stu-id="a20ee-203">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="a20ee-204">ID do link</span><span class="sxs-lookup"><span data-stu-id="a20ee-204">Link-Id</span></span>                | \-           |
| <span data-ttu-id="a20ee-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a20ee-205">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="a20ee-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="a20ee-206">System-Only</span></span>            | <span data-ttu-id="a20ee-207">True</span><span class="sxs-lookup"><span data-stu-id="a20ee-207">True</span></span>         |
| <span data-ttu-id="a20ee-208">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a20ee-208">Is-Single-Valued</span></span>       | <span data-ttu-id="a20ee-209">True</span><span class="sxs-lookup"><span data-stu-id="a20ee-209">True</span></span>         |
| <span data-ttu-id="a20ee-210">É indexado</span><span class="sxs-lookup"><span data-stu-id="a20ee-210">Is Indexed</span></span>             | <span data-ttu-id="a20ee-211">Falso</span><span class="sxs-lookup"><span data-stu-id="a20ee-211">False</span></span>        |
| <span data-ttu-id="a20ee-212">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a20ee-212">In Global Catalog</span></span>      | <span data-ttu-id="a20ee-213">Falso</span><span class="sxs-lookup"><span data-stu-id="a20ee-213">False</span></span>        |
| <span data-ttu-id="a20ee-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a20ee-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="a20ee-215">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a20ee-215">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="a20ee-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a20ee-216">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="a20ee-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a20ee-217">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="a20ee-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a20ee-218">Search-Flags</span></span>           | <span data-ttu-id="a20ee-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a20ee-219">0x00000000</span></span>   |
| <span data-ttu-id="a20ee-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a20ee-220">System-Flags</span></span>           | <span data-ttu-id="a20ee-221">0x08000014</span><span class="sxs-lookup"><span data-stu-id="a20ee-221">0x08000014</span></span>   |
| <span data-ttu-id="a20ee-222">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a20ee-222">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="a20ee-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a20ee-223">Windows Server 2008</span></span>



| <span data-ttu-id="a20ee-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="a20ee-224">Entry</span></span> | <span data-ttu-id="a20ee-225">Valor</span><span class="sxs-lookup"><span data-stu-id="a20ee-225">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="a20ee-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="a20ee-226">Link-Id</span></span>                | \-           |
| <span data-ttu-id="a20ee-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a20ee-227">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="a20ee-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="a20ee-228">System-Only</span></span>            | <span data-ttu-id="a20ee-229">True</span><span class="sxs-lookup"><span data-stu-id="a20ee-229">True</span></span>         |
| <span data-ttu-id="a20ee-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a20ee-230">Is-Single-Valued</span></span>       | <span data-ttu-id="a20ee-231">True</span><span class="sxs-lookup"><span data-stu-id="a20ee-231">True</span></span>         |
| <span data-ttu-id="a20ee-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="a20ee-232">Is Indexed</span></span>             | <span data-ttu-id="a20ee-233">Falso</span><span class="sxs-lookup"><span data-stu-id="a20ee-233">False</span></span>        |
| <span data-ttu-id="a20ee-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a20ee-234">In Global Catalog</span></span>      | <span data-ttu-id="a20ee-235">Falso</span><span class="sxs-lookup"><span data-stu-id="a20ee-235">False</span></span>        |
| <span data-ttu-id="a20ee-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a20ee-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="a20ee-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a20ee-237">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="a20ee-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a20ee-238">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="a20ee-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a20ee-239">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="a20ee-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a20ee-240">Search-Flags</span></span>           | <span data-ttu-id="a20ee-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a20ee-241">0x00000000</span></span>   |
| <span data-ttu-id="a20ee-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a20ee-242">System-Flags</span></span>           | <span data-ttu-id="a20ee-243">0x08000014</span><span class="sxs-lookup"><span data-stu-id="a20ee-243">0x08000014</span></span>   |
| <span data-ttu-id="a20ee-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a20ee-244">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a20ee-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a20ee-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a20ee-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="a20ee-246">Entry</span></span> | <span data-ttu-id="a20ee-247">Valor</span><span class="sxs-lookup"><span data-stu-id="a20ee-247">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="a20ee-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="a20ee-248">Link-Id</span></span>                | \-           |
| <span data-ttu-id="a20ee-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a20ee-249">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="a20ee-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="a20ee-250">System-Only</span></span>            | <span data-ttu-id="a20ee-251">True</span><span class="sxs-lookup"><span data-stu-id="a20ee-251">True</span></span>         |
| <span data-ttu-id="a20ee-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a20ee-252">Is-Single-Valued</span></span>       | <span data-ttu-id="a20ee-253">True</span><span class="sxs-lookup"><span data-stu-id="a20ee-253">True</span></span>         |
| <span data-ttu-id="a20ee-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="a20ee-254">Is Indexed</span></span>             | <span data-ttu-id="a20ee-255">Falso</span><span class="sxs-lookup"><span data-stu-id="a20ee-255">False</span></span>        |
| <span data-ttu-id="a20ee-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a20ee-256">In Global Catalog</span></span>      | <span data-ttu-id="a20ee-257">Falso</span><span class="sxs-lookup"><span data-stu-id="a20ee-257">False</span></span>        |
| <span data-ttu-id="a20ee-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a20ee-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="a20ee-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a20ee-259">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="a20ee-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a20ee-260">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="a20ee-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a20ee-261">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="a20ee-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a20ee-262">Search-Flags</span></span>           | <span data-ttu-id="a20ee-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a20ee-263">0x00000000</span></span>   |
| <span data-ttu-id="a20ee-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a20ee-264">System-Flags</span></span>           | <span data-ttu-id="a20ee-265">0x08000014</span><span class="sxs-lookup"><span data-stu-id="a20ee-265">0x08000014</span></span>   |
| <span data-ttu-id="a20ee-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a20ee-266">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="a20ee-267">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a20ee-267">Windows Server 2012</span></span>



| <span data-ttu-id="a20ee-268">Entrada</span><span class="sxs-lookup"><span data-stu-id="a20ee-268">Entry</span></span> | <span data-ttu-id="a20ee-269">Valor</span><span class="sxs-lookup"><span data-stu-id="a20ee-269">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="a20ee-270">ID do link</span><span class="sxs-lookup"><span data-stu-id="a20ee-270">Link-Id</span></span>                | \-           |
| <span data-ttu-id="a20ee-271">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a20ee-271">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="a20ee-272">System-Only</span><span class="sxs-lookup"><span data-stu-id="a20ee-272">System-Only</span></span>            | <span data-ttu-id="a20ee-273">True</span><span class="sxs-lookup"><span data-stu-id="a20ee-273">True</span></span>         |
| <span data-ttu-id="a20ee-274">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a20ee-274">Is-Single-Valued</span></span>       | <span data-ttu-id="a20ee-275">True</span><span class="sxs-lookup"><span data-stu-id="a20ee-275">True</span></span>         |
| <span data-ttu-id="a20ee-276">É indexado</span><span class="sxs-lookup"><span data-stu-id="a20ee-276">Is Indexed</span></span>             | <span data-ttu-id="a20ee-277">Falso</span><span class="sxs-lookup"><span data-stu-id="a20ee-277">False</span></span>        |
| <span data-ttu-id="a20ee-278">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a20ee-278">In Global Catalog</span></span>      | <span data-ttu-id="a20ee-279">Falso</span><span class="sxs-lookup"><span data-stu-id="a20ee-279">False</span></span>        |
| <span data-ttu-id="a20ee-280">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a20ee-280">NT-Security-Descriptor</span></span> | <span data-ttu-id="a20ee-281">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a20ee-281">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="a20ee-282">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a20ee-282">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="a20ee-283">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a20ee-283">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="a20ee-284">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a20ee-284">Search-Flags</span></span>           | <span data-ttu-id="a20ee-285">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a20ee-285">0x00000000</span></span>   |
| <span data-ttu-id="a20ee-286">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a20ee-286">System-Flags</span></span>           | <span data-ttu-id="a20ee-287">0x08000014</span><span class="sxs-lookup"><span data-stu-id="a20ee-287">0x08000014</span></span>   |
| <span data-ttu-id="a20ee-288">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a20ee-288">Classes used in</span></span>        | \-           |



 

 




