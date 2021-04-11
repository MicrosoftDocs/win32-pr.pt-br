---
title: Atributo Sync-with-SID
description: Para a sincronização de diretiva local/objeto de grupo do SAM Builtin, esse é o grupo local ao qual um objeto corresponde.
ms.assetid: b983210d-1c54-4355-bc37-771e51016175
ms.tgt_platform: multiple
keywords:
- Atributo sincronizar-com-SID esquema do AD
- Esquema de AD do atributo syncWithSID
topic_type:
- apiref
api_name:
- Sync-With-SID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 845a95b737a56a853fa7fb4e77d5612f1efc3c37
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086984"
---
# <a name="sync-with-sid-attribute"></a><span data-ttu-id="21b4a-105">Atributo Sync-with-SID</span><span class="sxs-lookup"><span data-stu-id="21b4a-105">Sync-With-SID attribute</span></span>

<span data-ttu-id="21b4a-106">Para a sincronização de diretiva local/objeto de grupo do SAM Builtin, esse é o grupo local ao qual um objeto corresponde.</span><span class="sxs-lookup"><span data-stu-id="21b4a-106">For the SAM builtin group object/ local policy synchronization, this is the local group to which an object corresponds.</span></span>



| <span data-ttu-id="21b4a-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="21b4a-107">Entry</span></span> | <span data-ttu-id="21b4a-108">Valor</span><span class="sxs-lookup"><span data-stu-id="21b4a-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="21b4a-109">CN</span><span class="sxs-lookup"><span data-stu-id="21b4a-109">CN</span></span>                | <span data-ttu-id="21b4a-110">Sincronizar-com-SID</span><span class="sxs-lookup"><span data-stu-id="21b4a-110">Sync-With-SID</span></span>                        |
| <span data-ttu-id="21b4a-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="21b4a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="21b4a-112">syncWithSID</span><span class="sxs-lookup"><span data-stu-id="21b4a-112">syncWithSID</span></span>                          |
| <span data-ttu-id="21b4a-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="21b4a-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="21b4a-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="21b4a-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="21b4a-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="21b4a-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="21b4a-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="21b4a-116">Attribute-Id</span></span>      | <span data-ttu-id="21b4a-117">1.2.840.113556.1.4.667</span><span class="sxs-lookup"><span data-stu-id="21b4a-117">1.2.840.113556.1.4.667</span></span>               |
| <span data-ttu-id="21b4a-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="21b4a-118">System-Id-Guid</span></span>    | <span data-ttu-id="21b4a-119">037651e5-441d-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="21b4a-119">037651e5-441d-11d1-a9c3-0000f80367c1</span></span> |
| <span data-ttu-id="21b4a-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="21b4a-120">Syntax</span></span>            | [<span data-ttu-id="21b4a-121">**Cadeia de caracteres (SID)**</span><span class="sxs-lookup"><span data-stu-id="21b4a-121">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="21b4a-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="21b4a-122">Implementations</span></span>

-   [<span data-ttu-id="21b4a-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="21b4a-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="21b4a-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="21b4a-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="21b4a-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="21b4a-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="21b4a-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="21b4a-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="21b4a-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="21b4a-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="21b4a-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="21b4a-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="21b4a-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="21b4a-129">Windows 2000 Server</span></span>



| <span data-ttu-id="21b4a-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="21b4a-130">Entry</span></span> | <span data-ttu-id="21b4a-131">Valor</span><span class="sxs-lookup"><span data-stu-id="21b4a-131">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="21b4a-132">ID do link</span><span class="sxs-lookup"><span data-stu-id="21b4a-132">Link-Id</span></span>                | \-           |
| <span data-ttu-id="21b4a-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21b4a-133">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="21b4a-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="21b4a-134">System-Only</span></span>            | <span data-ttu-id="21b4a-135">Falso</span><span class="sxs-lookup"><span data-stu-id="21b4a-135">False</span></span>        |
| <span data-ttu-id="21b4a-136">É de valor único</span><span class="sxs-lookup"><span data-stu-id="21b4a-136">Is-Single-Valued</span></span>       | <span data-ttu-id="21b4a-137">True</span><span class="sxs-lookup"><span data-stu-id="21b4a-137">True</span></span>         |
| <span data-ttu-id="21b4a-138">É indexado</span><span class="sxs-lookup"><span data-stu-id="21b4a-138">Is Indexed</span></span>             | <span data-ttu-id="21b4a-139">Falso</span><span class="sxs-lookup"><span data-stu-id="21b4a-139">False</span></span>        |
| <span data-ttu-id="21b4a-140">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="21b4a-140">In Global Catalog</span></span>      | <span data-ttu-id="21b4a-141">Falso</span><span class="sxs-lookup"><span data-stu-id="21b4a-141">False</span></span>        |
| <span data-ttu-id="21b4a-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="21b4a-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="21b4a-143">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="21b4a-143">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="21b4a-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21b4a-144">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="21b4a-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21b4a-145">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="21b4a-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21b4a-146">Search-Flags</span></span>           | <span data-ttu-id="21b4a-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21b4a-147">0x00000000</span></span>   |
| <span data-ttu-id="21b4a-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21b4a-148">System-Flags</span></span>           | <span data-ttu-id="21b4a-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21b4a-149">0x00000010</span></span>   |
| <span data-ttu-id="21b4a-150">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="21b4a-150">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003"></a><span data-ttu-id="21b4a-151">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="21b4a-151">Windows Server 2003</span></span>



| <span data-ttu-id="21b4a-152">Entrada</span><span class="sxs-lookup"><span data-stu-id="21b4a-152">Entry</span></span> | <span data-ttu-id="21b4a-153">Valor</span><span class="sxs-lookup"><span data-stu-id="21b4a-153">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="21b4a-154">ID do link</span><span class="sxs-lookup"><span data-stu-id="21b4a-154">Link-Id</span></span>                | \-           |
| <span data-ttu-id="21b4a-155">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21b4a-155">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="21b4a-156">System-Only</span><span class="sxs-lookup"><span data-stu-id="21b4a-156">System-Only</span></span>            | <span data-ttu-id="21b4a-157">Falso</span><span class="sxs-lookup"><span data-stu-id="21b4a-157">False</span></span>        |
| <span data-ttu-id="21b4a-158">É de valor único</span><span class="sxs-lookup"><span data-stu-id="21b4a-158">Is-Single-Valued</span></span>       | <span data-ttu-id="21b4a-159">True</span><span class="sxs-lookup"><span data-stu-id="21b4a-159">True</span></span>         |
| <span data-ttu-id="21b4a-160">É indexado</span><span class="sxs-lookup"><span data-stu-id="21b4a-160">Is Indexed</span></span>             | <span data-ttu-id="21b4a-161">Falso</span><span class="sxs-lookup"><span data-stu-id="21b4a-161">False</span></span>        |
| <span data-ttu-id="21b4a-162">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="21b4a-162">In Global Catalog</span></span>      | <span data-ttu-id="21b4a-163">Falso</span><span class="sxs-lookup"><span data-stu-id="21b4a-163">False</span></span>        |
| <span data-ttu-id="21b4a-164">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="21b4a-164">NT-Security-Descriptor</span></span> | <span data-ttu-id="21b4a-165">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="21b4a-165">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="21b4a-166">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21b4a-166">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="21b4a-167">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21b4a-167">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="21b4a-168">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21b4a-168">Search-Flags</span></span>           | <span data-ttu-id="21b4a-169">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21b4a-169">0x00000000</span></span>   |
| <span data-ttu-id="21b4a-170">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21b4a-170">System-Flags</span></span>           | <span data-ttu-id="21b4a-171">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21b4a-171">0x00000010</span></span>   |
| <span data-ttu-id="21b4a-172">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="21b4a-172">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="21b4a-173">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="21b4a-173">Windows Server 2003 R2</span></span>



| <span data-ttu-id="21b4a-174">Entrada</span><span class="sxs-lookup"><span data-stu-id="21b4a-174">Entry</span></span> | <span data-ttu-id="21b4a-175">Valor</span><span class="sxs-lookup"><span data-stu-id="21b4a-175">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="21b4a-176">ID do link</span><span class="sxs-lookup"><span data-stu-id="21b4a-176">Link-Id</span></span>                | \-           |
| <span data-ttu-id="21b4a-177">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21b4a-177">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="21b4a-178">System-Only</span><span class="sxs-lookup"><span data-stu-id="21b4a-178">System-Only</span></span>            | <span data-ttu-id="21b4a-179">Falso</span><span class="sxs-lookup"><span data-stu-id="21b4a-179">False</span></span>        |
| <span data-ttu-id="21b4a-180">É de valor único</span><span class="sxs-lookup"><span data-stu-id="21b4a-180">Is-Single-Valued</span></span>       | <span data-ttu-id="21b4a-181">True</span><span class="sxs-lookup"><span data-stu-id="21b4a-181">True</span></span>         |
| <span data-ttu-id="21b4a-182">É indexado</span><span class="sxs-lookup"><span data-stu-id="21b4a-182">Is Indexed</span></span>             | <span data-ttu-id="21b4a-183">Falso</span><span class="sxs-lookup"><span data-stu-id="21b4a-183">False</span></span>        |
| <span data-ttu-id="21b4a-184">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="21b4a-184">In Global Catalog</span></span>      | <span data-ttu-id="21b4a-185">Falso</span><span class="sxs-lookup"><span data-stu-id="21b4a-185">False</span></span>        |
| <span data-ttu-id="21b4a-186">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="21b4a-186">NT-Security-Descriptor</span></span> | <span data-ttu-id="21b4a-187">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="21b4a-187">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="21b4a-188">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21b4a-188">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="21b4a-189">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21b4a-189">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="21b4a-190">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21b4a-190">Search-Flags</span></span>           | <span data-ttu-id="21b4a-191">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21b4a-191">0x00000000</span></span>   |
| <span data-ttu-id="21b4a-192">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21b4a-192">System-Flags</span></span>           | <span data-ttu-id="21b4a-193">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21b4a-193">0x00000010</span></span>   |
| <span data-ttu-id="21b4a-194">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="21b4a-194">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="21b4a-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21b4a-195">Windows Server 2008</span></span>



| <span data-ttu-id="21b4a-196">Entrada</span><span class="sxs-lookup"><span data-stu-id="21b4a-196">Entry</span></span> | <span data-ttu-id="21b4a-197">Valor</span><span class="sxs-lookup"><span data-stu-id="21b4a-197">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="21b4a-198">ID do link</span><span class="sxs-lookup"><span data-stu-id="21b4a-198">Link-Id</span></span>                | \-           |
| <span data-ttu-id="21b4a-199">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21b4a-199">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="21b4a-200">System-Only</span><span class="sxs-lookup"><span data-stu-id="21b4a-200">System-Only</span></span>            | <span data-ttu-id="21b4a-201">Falso</span><span class="sxs-lookup"><span data-stu-id="21b4a-201">False</span></span>        |
| <span data-ttu-id="21b4a-202">É de valor único</span><span class="sxs-lookup"><span data-stu-id="21b4a-202">Is-Single-Valued</span></span>       | <span data-ttu-id="21b4a-203">True</span><span class="sxs-lookup"><span data-stu-id="21b4a-203">True</span></span>         |
| <span data-ttu-id="21b4a-204">É indexado</span><span class="sxs-lookup"><span data-stu-id="21b4a-204">Is Indexed</span></span>             | <span data-ttu-id="21b4a-205">Falso</span><span class="sxs-lookup"><span data-stu-id="21b4a-205">False</span></span>        |
| <span data-ttu-id="21b4a-206">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="21b4a-206">In Global Catalog</span></span>      | <span data-ttu-id="21b4a-207">Falso</span><span class="sxs-lookup"><span data-stu-id="21b4a-207">False</span></span>        |
| <span data-ttu-id="21b4a-208">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="21b4a-208">NT-Security-Descriptor</span></span> | <span data-ttu-id="21b4a-209">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="21b4a-209">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="21b4a-210">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21b4a-210">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="21b4a-211">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21b4a-211">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="21b4a-212">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21b4a-212">Search-Flags</span></span>           | <span data-ttu-id="21b4a-213">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21b4a-213">0x00000000</span></span>   |
| <span data-ttu-id="21b4a-214">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21b4a-214">System-Flags</span></span>           | <span data-ttu-id="21b4a-215">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21b4a-215">0x00000010</span></span>   |
| <span data-ttu-id="21b4a-216">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="21b4a-216">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="21b4a-217">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="21b4a-217">Windows Server 2008 R2</span></span>



| <span data-ttu-id="21b4a-218">Entrada</span><span class="sxs-lookup"><span data-stu-id="21b4a-218">Entry</span></span> | <span data-ttu-id="21b4a-219">Valor</span><span class="sxs-lookup"><span data-stu-id="21b4a-219">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="21b4a-220">ID do link</span><span class="sxs-lookup"><span data-stu-id="21b4a-220">Link-Id</span></span>                | \-           |
| <span data-ttu-id="21b4a-221">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21b4a-221">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="21b4a-222">System-Only</span><span class="sxs-lookup"><span data-stu-id="21b4a-222">System-Only</span></span>            | <span data-ttu-id="21b4a-223">Falso</span><span class="sxs-lookup"><span data-stu-id="21b4a-223">False</span></span>        |
| <span data-ttu-id="21b4a-224">É de valor único</span><span class="sxs-lookup"><span data-stu-id="21b4a-224">Is-Single-Valued</span></span>       | <span data-ttu-id="21b4a-225">True</span><span class="sxs-lookup"><span data-stu-id="21b4a-225">True</span></span>         |
| <span data-ttu-id="21b4a-226">É indexado</span><span class="sxs-lookup"><span data-stu-id="21b4a-226">Is Indexed</span></span>             | <span data-ttu-id="21b4a-227">Falso</span><span class="sxs-lookup"><span data-stu-id="21b4a-227">False</span></span>        |
| <span data-ttu-id="21b4a-228">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="21b4a-228">In Global Catalog</span></span>      | <span data-ttu-id="21b4a-229">Falso</span><span class="sxs-lookup"><span data-stu-id="21b4a-229">False</span></span>        |
| <span data-ttu-id="21b4a-230">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="21b4a-230">NT-Security-Descriptor</span></span> | <span data-ttu-id="21b4a-231">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="21b4a-231">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="21b4a-232">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21b4a-232">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="21b4a-233">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21b4a-233">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="21b4a-234">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21b4a-234">Search-Flags</span></span>           | <span data-ttu-id="21b4a-235">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21b4a-235">0x00000000</span></span>   |
| <span data-ttu-id="21b4a-236">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21b4a-236">System-Flags</span></span>           | <span data-ttu-id="21b4a-237">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21b4a-237">0x00000010</span></span>   |
| <span data-ttu-id="21b4a-238">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="21b4a-238">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="21b4a-239">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="21b4a-239">Windows Server 2012</span></span>



| <span data-ttu-id="21b4a-240">Entrada</span><span class="sxs-lookup"><span data-stu-id="21b4a-240">Entry</span></span> | <span data-ttu-id="21b4a-241">Valor</span><span class="sxs-lookup"><span data-stu-id="21b4a-241">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="21b4a-242">ID do link</span><span class="sxs-lookup"><span data-stu-id="21b4a-242">Link-Id</span></span>                | \-           |
| <span data-ttu-id="21b4a-243">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21b4a-243">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="21b4a-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="21b4a-244">System-Only</span></span>            | <span data-ttu-id="21b4a-245">Falso</span><span class="sxs-lookup"><span data-stu-id="21b4a-245">False</span></span>        |
| <span data-ttu-id="21b4a-246">É de valor único</span><span class="sxs-lookup"><span data-stu-id="21b4a-246">Is-Single-Valued</span></span>       | <span data-ttu-id="21b4a-247">True</span><span class="sxs-lookup"><span data-stu-id="21b4a-247">True</span></span>         |
| <span data-ttu-id="21b4a-248">É indexado</span><span class="sxs-lookup"><span data-stu-id="21b4a-248">Is Indexed</span></span>             | <span data-ttu-id="21b4a-249">Falso</span><span class="sxs-lookup"><span data-stu-id="21b4a-249">False</span></span>        |
| <span data-ttu-id="21b4a-250">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="21b4a-250">In Global Catalog</span></span>      | <span data-ttu-id="21b4a-251">Falso</span><span class="sxs-lookup"><span data-stu-id="21b4a-251">False</span></span>        |
| <span data-ttu-id="21b4a-252">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="21b4a-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="21b4a-253">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="21b4a-253">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="21b4a-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21b4a-254">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="21b4a-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21b4a-255">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="21b4a-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21b4a-256">Search-Flags</span></span>           | <span data-ttu-id="21b4a-257">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21b4a-257">0x00000000</span></span>   |
| <span data-ttu-id="21b4a-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21b4a-258">System-Flags</span></span>           | <span data-ttu-id="21b4a-259">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21b4a-259">0x00000010</span></span>   |
| <span data-ttu-id="21b4a-260">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="21b4a-260">Classes used in</span></span>        | \-           |



 

 




