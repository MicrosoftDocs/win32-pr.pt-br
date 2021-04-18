---
title: Atributo DN-Reference-Update
description: Se um objeto for renomeado, esse atributo será usado para rastrear todos os nomes anteriores e atuais que foram atribuídos a um objeto para que os objetos vinculados ainda possam encontrá-lo.
ms.assetid: 28e02a38-eed8-475c-a381-145857477ec6
ms.tgt_platform: multiple
keywords:
- DN-Reference-atualizar o atributo AD Schema
- Esquema de AD do atributo dNReferenceUpdate
topic_type:
- apiref
api_name:
- DN-Reference-Update
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71e8360be6e7ed6697363daa0f6ff32e2ec5fb9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105752978"
---
# <a name="dn-reference-update-attribute"></a><span data-ttu-id="7656e-105">Atributo DN-Reference-Update</span><span class="sxs-lookup"><span data-stu-id="7656e-105">DN-Reference-Update attribute</span></span>

<span data-ttu-id="7656e-106">Se um objeto for renomeado, esse atributo será usado para rastrear todos os nomes anteriores e atuais que foram atribuídos a um objeto para que os objetos vinculados ainda possam encontrá-lo.</span><span class="sxs-lookup"><span data-stu-id="7656e-106">If an object is renamed, this attribute is used to track all of the previous and current names that have been assigned to an object so that linked objects can still find it.</span></span>



| <span data-ttu-id="7656e-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="7656e-107">Entry</span></span> | <span data-ttu-id="7656e-108">Valor</span><span class="sxs-lookup"><span data-stu-id="7656e-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="7656e-109">CN</span><span class="sxs-lookup"><span data-stu-id="7656e-109">CN</span></span>                | <span data-ttu-id="7656e-110">DN-referência-atualização</span><span class="sxs-lookup"><span data-stu-id="7656e-110">DN-Reference-Update</span></span>                     |
| <span data-ttu-id="7656e-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7656e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7656e-112">dNReferenceUpdate</span><span class="sxs-lookup"><span data-stu-id="7656e-112">dNReferenceUpdate</span></span>                       |
| <span data-ttu-id="7656e-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="7656e-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="7656e-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="7656e-114">Update Privilege</span></span>  | <span data-ttu-id="7656e-115">Isso é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="7656e-115">This is set by the system.</span></span>              |
| <span data-ttu-id="7656e-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="7656e-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="7656e-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7656e-117">Attribute-Id</span></span>      | <span data-ttu-id="7656e-118">1.2.840.113556.1.4.1242</span><span class="sxs-lookup"><span data-stu-id="7656e-118">1.2.840.113556.1.4.1242</span></span>                 |
| <span data-ttu-id="7656e-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7656e-119">System-Id-Guid</span></span>    | <span data-ttu-id="7656e-120">2df90d86-009f-11d2-aa4c-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="7656e-120">2df90d86-009f-11d2-aa4c-00c04fd7d83a</span></span>    |
| <span data-ttu-id="7656e-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="7656e-121">Syntax</span></span>            | [<span data-ttu-id="7656e-122">**Objeto (DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="7656e-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="7656e-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="7656e-123">Implementations</span></span>

-   [<span data-ttu-id="7656e-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7656e-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7656e-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7656e-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7656e-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7656e-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7656e-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7656e-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7656e-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7656e-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7656e-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7656e-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7656e-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7656e-130">Windows 2000 Server</span></span>



| <span data-ttu-id="7656e-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="7656e-131">Entry</span></span> | <span data-ttu-id="7656e-132">Valor</span><span class="sxs-lookup"><span data-stu-id="7656e-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="7656e-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="7656e-133">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="7656e-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7656e-134">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="7656e-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="7656e-135">System-Only</span></span>            | <span data-ttu-id="7656e-136">True</span><span class="sxs-lookup"><span data-stu-id="7656e-136">True</span></span>                                                               |
| <span data-ttu-id="7656e-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7656e-137">Is-Single-Valued</span></span>       | <span data-ttu-id="7656e-138">Falso</span><span class="sxs-lookup"><span data-stu-id="7656e-138">False</span></span>                                                              |
| <span data-ttu-id="7656e-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="7656e-139">Is Indexed</span></span>             | <span data-ttu-id="7656e-140">Falso</span><span class="sxs-lookup"><span data-stu-id="7656e-140">False</span></span>                                                              |
| <span data-ttu-id="7656e-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7656e-141">In Global Catalog</span></span>      | <span data-ttu-id="7656e-142">Falso</span><span class="sxs-lookup"><span data-stu-id="7656e-142">False</span></span>                                                              |
| <span data-ttu-id="7656e-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7656e-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="7656e-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7656e-144">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="7656e-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7656e-145">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="7656e-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7656e-146">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="7656e-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7656e-147">Search-Flags</span></span>           | <span data-ttu-id="7656e-148">0x00000008</span><span class="sxs-lookup"><span data-stu-id="7656e-148">0x00000008</span></span>                                                         |
| <span data-ttu-id="7656e-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7656e-149">System-Flags</span></span>           | <span data-ttu-id="7656e-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7656e-150">0x00000010</span></span>                                                         |
| <span data-ttu-id="7656e-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7656e-151">Classes used in</span></span>        | [<span data-ttu-id="7656e-152">**Infraestrutura – atualização**</span><span class="sxs-lookup"><span data-stu-id="7656e-152">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7656e-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7656e-153">Windows Server 2003</span></span>



| <span data-ttu-id="7656e-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="7656e-154">Entry</span></span> | <span data-ttu-id="7656e-155">Valor</span><span class="sxs-lookup"><span data-stu-id="7656e-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="7656e-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="7656e-156">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="7656e-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7656e-157">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="7656e-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="7656e-158">System-Only</span></span>            | <span data-ttu-id="7656e-159">True</span><span class="sxs-lookup"><span data-stu-id="7656e-159">True</span></span>                                                               |
| <span data-ttu-id="7656e-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7656e-160">Is-Single-Valued</span></span>       | <span data-ttu-id="7656e-161">Falso</span><span class="sxs-lookup"><span data-stu-id="7656e-161">False</span></span>                                                              |
| <span data-ttu-id="7656e-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="7656e-162">Is Indexed</span></span>             | <span data-ttu-id="7656e-163">Falso</span><span class="sxs-lookup"><span data-stu-id="7656e-163">False</span></span>                                                              |
| <span data-ttu-id="7656e-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7656e-164">In Global Catalog</span></span>      | <span data-ttu-id="7656e-165">Falso</span><span class="sxs-lookup"><span data-stu-id="7656e-165">False</span></span>                                                              |
| <span data-ttu-id="7656e-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7656e-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="7656e-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7656e-167">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="7656e-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7656e-168">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="7656e-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7656e-169">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="7656e-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7656e-170">Search-Flags</span></span>           | <span data-ttu-id="7656e-171">0x00000008</span><span class="sxs-lookup"><span data-stu-id="7656e-171">0x00000008</span></span>                                                         |
| <span data-ttu-id="7656e-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7656e-172">System-Flags</span></span>           | <span data-ttu-id="7656e-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7656e-173">0x00000010</span></span>                                                         |
| <span data-ttu-id="7656e-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7656e-174">Classes used in</span></span>        | [<span data-ttu-id="7656e-175">**Infraestrutura – atualização**</span><span class="sxs-lookup"><span data-stu-id="7656e-175">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7656e-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7656e-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7656e-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="7656e-177">Entry</span></span> | <span data-ttu-id="7656e-178">Valor</span><span class="sxs-lookup"><span data-stu-id="7656e-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="7656e-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="7656e-179">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="7656e-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7656e-180">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="7656e-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="7656e-181">System-Only</span></span>            | <span data-ttu-id="7656e-182">True</span><span class="sxs-lookup"><span data-stu-id="7656e-182">True</span></span>                                                               |
| <span data-ttu-id="7656e-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7656e-183">Is-Single-Valued</span></span>       | <span data-ttu-id="7656e-184">Falso</span><span class="sxs-lookup"><span data-stu-id="7656e-184">False</span></span>                                                              |
| <span data-ttu-id="7656e-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="7656e-185">Is Indexed</span></span>             | <span data-ttu-id="7656e-186">Falso</span><span class="sxs-lookup"><span data-stu-id="7656e-186">False</span></span>                                                              |
| <span data-ttu-id="7656e-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7656e-187">In Global Catalog</span></span>      | <span data-ttu-id="7656e-188">Falso</span><span class="sxs-lookup"><span data-stu-id="7656e-188">False</span></span>                                                              |
| <span data-ttu-id="7656e-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7656e-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="7656e-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7656e-190">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="7656e-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7656e-191">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="7656e-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7656e-192">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="7656e-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7656e-193">Search-Flags</span></span>           | <span data-ttu-id="7656e-194">0x00000008</span><span class="sxs-lookup"><span data-stu-id="7656e-194">0x00000008</span></span>                                                         |
| <span data-ttu-id="7656e-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7656e-195">System-Flags</span></span>           | <span data-ttu-id="7656e-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7656e-196">0x00000010</span></span>                                                         |
| <span data-ttu-id="7656e-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7656e-197">Classes used in</span></span>        | [<span data-ttu-id="7656e-198">**Infraestrutura – atualização**</span><span class="sxs-lookup"><span data-stu-id="7656e-198">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7656e-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7656e-199">Windows Server 2008</span></span>



| <span data-ttu-id="7656e-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="7656e-200">Entry</span></span> | <span data-ttu-id="7656e-201">Valor</span><span class="sxs-lookup"><span data-stu-id="7656e-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="7656e-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="7656e-202">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="7656e-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7656e-203">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="7656e-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="7656e-204">System-Only</span></span>            | <span data-ttu-id="7656e-205">True</span><span class="sxs-lookup"><span data-stu-id="7656e-205">True</span></span>                                                               |
| <span data-ttu-id="7656e-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7656e-206">Is-Single-Valued</span></span>       | <span data-ttu-id="7656e-207">Falso</span><span class="sxs-lookup"><span data-stu-id="7656e-207">False</span></span>                                                              |
| <span data-ttu-id="7656e-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="7656e-208">Is Indexed</span></span>             | <span data-ttu-id="7656e-209">Falso</span><span class="sxs-lookup"><span data-stu-id="7656e-209">False</span></span>                                                              |
| <span data-ttu-id="7656e-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7656e-210">In Global Catalog</span></span>      | <span data-ttu-id="7656e-211">Falso</span><span class="sxs-lookup"><span data-stu-id="7656e-211">False</span></span>                                                              |
| <span data-ttu-id="7656e-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7656e-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="7656e-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7656e-213">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="7656e-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7656e-214">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="7656e-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7656e-215">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="7656e-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7656e-216">Search-Flags</span></span>           | <span data-ttu-id="7656e-217">0x00000008</span><span class="sxs-lookup"><span data-stu-id="7656e-217">0x00000008</span></span>                                                         |
| <span data-ttu-id="7656e-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7656e-218">System-Flags</span></span>           | <span data-ttu-id="7656e-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7656e-219">0x00000010</span></span>                                                         |
| <span data-ttu-id="7656e-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7656e-220">Classes used in</span></span>        | [<span data-ttu-id="7656e-221">**Infraestrutura – atualização**</span><span class="sxs-lookup"><span data-stu-id="7656e-221">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7656e-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7656e-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7656e-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="7656e-223">Entry</span></span> | <span data-ttu-id="7656e-224">Valor</span><span class="sxs-lookup"><span data-stu-id="7656e-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="7656e-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="7656e-225">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="7656e-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7656e-226">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="7656e-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="7656e-227">System-Only</span></span>            | <span data-ttu-id="7656e-228">True</span><span class="sxs-lookup"><span data-stu-id="7656e-228">True</span></span>                                                               |
| <span data-ttu-id="7656e-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7656e-229">Is-Single-Valued</span></span>       | <span data-ttu-id="7656e-230">Falso</span><span class="sxs-lookup"><span data-stu-id="7656e-230">False</span></span>                                                              |
| <span data-ttu-id="7656e-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="7656e-231">Is Indexed</span></span>             | <span data-ttu-id="7656e-232">Falso</span><span class="sxs-lookup"><span data-stu-id="7656e-232">False</span></span>                                                              |
| <span data-ttu-id="7656e-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7656e-233">In Global Catalog</span></span>      | <span data-ttu-id="7656e-234">Falso</span><span class="sxs-lookup"><span data-stu-id="7656e-234">False</span></span>                                                              |
| <span data-ttu-id="7656e-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7656e-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="7656e-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7656e-236">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="7656e-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7656e-237">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="7656e-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7656e-238">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="7656e-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7656e-239">Search-Flags</span></span>           | <span data-ttu-id="7656e-240">0x00000008</span><span class="sxs-lookup"><span data-stu-id="7656e-240">0x00000008</span></span>                                                         |
| <span data-ttu-id="7656e-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7656e-241">System-Flags</span></span>           | <span data-ttu-id="7656e-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7656e-242">0x00000010</span></span>                                                         |
| <span data-ttu-id="7656e-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7656e-243">Classes used in</span></span>        | [<span data-ttu-id="7656e-244">**Infraestrutura – atualização**</span><span class="sxs-lookup"><span data-stu-id="7656e-244">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7656e-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7656e-245">Windows Server 2012</span></span>



| <span data-ttu-id="7656e-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="7656e-246">Entry</span></span> | <span data-ttu-id="7656e-247">Valor</span><span class="sxs-lookup"><span data-stu-id="7656e-247">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="7656e-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="7656e-248">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="7656e-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7656e-249">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="7656e-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="7656e-250">System-Only</span></span>            | <span data-ttu-id="7656e-251">True</span><span class="sxs-lookup"><span data-stu-id="7656e-251">True</span></span>                                                               |
| <span data-ttu-id="7656e-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7656e-252">Is-Single-Valued</span></span>       | <span data-ttu-id="7656e-253">Falso</span><span class="sxs-lookup"><span data-stu-id="7656e-253">False</span></span>                                                              |
| <span data-ttu-id="7656e-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="7656e-254">Is Indexed</span></span>             | <span data-ttu-id="7656e-255">Falso</span><span class="sxs-lookup"><span data-stu-id="7656e-255">False</span></span>                                                              |
| <span data-ttu-id="7656e-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7656e-256">In Global Catalog</span></span>      | <span data-ttu-id="7656e-257">Falso</span><span class="sxs-lookup"><span data-stu-id="7656e-257">False</span></span>                                                              |
| <span data-ttu-id="7656e-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7656e-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="7656e-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7656e-259">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="7656e-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7656e-260">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="7656e-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7656e-261">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="7656e-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7656e-262">Search-Flags</span></span>           | <span data-ttu-id="7656e-263">0x00000008</span><span class="sxs-lookup"><span data-stu-id="7656e-263">0x00000008</span></span>                                                         |
| <span data-ttu-id="7656e-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7656e-264">System-Flags</span></span>           | <span data-ttu-id="7656e-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7656e-265">0x00000010</span></span>                                                         |
| <span data-ttu-id="7656e-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7656e-266">Classes used in</span></span>        | [<span data-ttu-id="7656e-267">**Infraestrutura – atualização**</span><span class="sxs-lookup"><span data-stu-id="7656e-267">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



 

 





