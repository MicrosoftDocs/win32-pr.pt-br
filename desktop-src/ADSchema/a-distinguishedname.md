---
title: Atributo obj-dist-Name
description: O mesmo que o nome distinto de um objeto. Usado pelo Exchange.
ms.assetid: 0dc2855c-2707-49d8-80e6-27f163a59bc8
ms.tgt_platform: multiple
keywords:
- Obj-dist-Name atributo AD Schema
- Esquema de AD do atributo distinguishedName
topic_type:
- apiref
api_name:
- Obj-Dist-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42cd118f38de78546b7b792bca3c8c9ef6d229cb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103824963"
---
# <a name="obj-dist-name-attribute"></a><span data-ttu-id="3645f-106">Atributo obj-dist-Name</span><span class="sxs-lookup"><span data-stu-id="3645f-106">Obj-Dist-Name attribute</span></span>

<span data-ttu-id="3645f-107">O mesmo que o nome distinto de um objeto.</span><span class="sxs-lookup"><span data-stu-id="3645f-107">Same as the Distinguished Name for an object.</span></span> <span data-ttu-id="3645f-108">Usado pelo Exchange.</span><span class="sxs-lookup"><span data-stu-id="3645f-108">Used by Exchange.</span></span>



| <span data-ttu-id="3645f-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="3645f-109">Entry</span></span> | <span data-ttu-id="3645f-110">Valor</span><span class="sxs-lookup"><span data-stu-id="3645f-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="3645f-111">CN</span><span class="sxs-lookup"><span data-stu-id="3645f-111">CN</span></span>                | <span data-ttu-id="3645f-112">Obj-dist-Name</span><span class="sxs-lookup"><span data-stu-id="3645f-112">Obj-Dist-Name</span></span>                           |
| <span data-ttu-id="3645f-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3645f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="3645f-114">distinguishedName</span><span class="sxs-lookup"><span data-stu-id="3645f-114">distinguishedName</span></span>                       |
| <span data-ttu-id="3645f-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="3645f-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="3645f-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="3645f-116">Update Privilege</span></span>  | <span data-ttu-id="3645f-117">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="3645f-117">This value is set by the system.</span></span>        |
| <span data-ttu-id="3645f-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="3645f-118">Update Frequency</span></span>  | <span data-ttu-id="3645f-119">Sempre que um objeto é criado ou movido.</span><span class="sxs-lookup"><span data-stu-id="3645f-119">Whenever an object is created or moved.</span></span> |
| <span data-ttu-id="3645f-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3645f-120">Attribute-Id</span></span>      | <span data-ttu-id="3645f-121">2.5.4.49</span><span class="sxs-lookup"><span data-stu-id="3645f-121">2.5.4.49</span></span>                                |
| <span data-ttu-id="3645f-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3645f-122">System-Id-Guid</span></span>    | <span data-ttu-id="3645f-123">bf9679e4-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="3645f-123">bf9679e4-0de6-11d0-a285-00aa003049e2</span></span>    |
| <span data-ttu-id="3645f-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="3645f-124">Syntax</span></span>            | [<span data-ttu-id="3645f-125">**Objeto (DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="3645f-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="3645f-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="3645f-126">Implementations</span></span>

-   [<span data-ttu-id="3645f-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3645f-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3645f-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3645f-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3645f-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="3645f-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="3645f-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3645f-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3645f-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3645f-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3645f-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3645f-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3645f-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3645f-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3645f-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3645f-134">Windows 2000 Server</span></span>



| <span data-ttu-id="3645f-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="3645f-135">Entry</span></span> | <span data-ttu-id="3645f-136">Valor</span><span class="sxs-lookup"><span data-stu-id="3645f-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3645f-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="3645f-137">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3645f-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3645f-138">MAPI-Id</span></span>                | <span data-ttu-id="3645f-139">0x803C</span><span class="sxs-lookup"><span data-stu-id="3645f-139">0x803C</span></span>                          |
| <span data-ttu-id="3645f-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="3645f-140">System-Only</span></span>            | <span data-ttu-id="3645f-141">True</span><span class="sxs-lookup"><span data-stu-id="3645f-141">True</span></span>                            |
| <span data-ttu-id="3645f-142">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3645f-142">Is-Single-Valued</span></span>       | <span data-ttu-id="3645f-143">True</span><span class="sxs-lookup"><span data-stu-id="3645f-143">True</span></span>                            |
| <span data-ttu-id="3645f-144">É indexado</span><span class="sxs-lookup"><span data-stu-id="3645f-144">Is Indexed</span></span>             | <span data-ttu-id="3645f-145">Falso</span><span class="sxs-lookup"><span data-stu-id="3645f-145">False</span></span>                           |
| <span data-ttu-id="3645f-146">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3645f-146">In Global Catalog</span></span>      | <span data-ttu-id="3645f-147">True</span><span class="sxs-lookup"><span data-stu-id="3645f-147">True</span></span>                            |
| <span data-ttu-id="3645f-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3645f-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="3645f-149">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3645f-149">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3645f-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3645f-150">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3645f-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3645f-151">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3645f-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3645f-152">Search-Flags</span></span>           | <span data-ttu-id="3645f-153">0x00000008</span><span class="sxs-lookup"><span data-stu-id="3645f-153">0x00000008</span></span>                      |
| <span data-ttu-id="3645f-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3645f-154">System-Flags</span></span>           | <span data-ttu-id="3645f-155">0x00000013</span><span class="sxs-lookup"><span data-stu-id="3645f-155">0x00000013</span></span>                      |
| <span data-ttu-id="3645f-156">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3645f-156">Classes used in</span></span>        | [<span data-ttu-id="3645f-157">**Início**</span><span class="sxs-lookup"><span data-stu-id="3645f-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3645f-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3645f-158">Windows Server 2003</span></span>



| <span data-ttu-id="3645f-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="3645f-159">Entry</span></span> | <span data-ttu-id="3645f-160">Valor</span><span class="sxs-lookup"><span data-stu-id="3645f-160">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3645f-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="3645f-161">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3645f-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3645f-162">MAPI-Id</span></span>                | <span data-ttu-id="3645f-163">0x803C</span><span class="sxs-lookup"><span data-stu-id="3645f-163">0x803C</span></span>                          |
| <span data-ttu-id="3645f-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="3645f-164">System-Only</span></span>            | <span data-ttu-id="3645f-165">True</span><span class="sxs-lookup"><span data-stu-id="3645f-165">True</span></span>                            |
| <span data-ttu-id="3645f-166">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3645f-166">Is-Single-Valued</span></span>       | <span data-ttu-id="3645f-167">True</span><span class="sxs-lookup"><span data-stu-id="3645f-167">True</span></span>                            |
| <span data-ttu-id="3645f-168">É indexado</span><span class="sxs-lookup"><span data-stu-id="3645f-168">Is Indexed</span></span>             | <span data-ttu-id="3645f-169">Falso</span><span class="sxs-lookup"><span data-stu-id="3645f-169">False</span></span>                           |
| <span data-ttu-id="3645f-170">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3645f-170">In Global Catalog</span></span>      | <span data-ttu-id="3645f-171">True</span><span class="sxs-lookup"><span data-stu-id="3645f-171">True</span></span>                            |
| <span data-ttu-id="3645f-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3645f-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="3645f-173">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3645f-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3645f-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3645f-174">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3645f-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3645f-175">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3645f-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3645f-176">Search-Flags</span></span>           | <span data-ttu-id="3645f-177">0x00000008</span><span class="sxs-lookup"><span data-stu-id="3645f-177">0x00000008</span></span>                      |
| <span data-ttu-id="3645f-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3645f-178">System-Flags</span></span>           | <span data-ttu-id="3645f-179">0x00000013</span><span class="sxs-lookup"><span data-stu-id="3645f-179">0x00000013</span></span>                      |
| <span data-ttu-id="3645f-180">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3645f-180">Classes used in</span></span>        | [<span data-ttu-id="3645f-181">**Início**</span><span class="sxs-lookup"><span data-stu-id="3645f-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="3645f-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="3645f-182">ADAM</span></span>



| <span data-ttu-id="3645f-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="3645f-183">Entry</span></span> | <span data-ttu-id="3645f-184">Valor</span><span class="sxs-lookup"><span data-stu-id="3645f-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3645f-185">ID do link</span><span class="sxs-lookup"><span data-stu-id="3645f-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3645f-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3645f-186">MAPI-Id</span></span>                | <span data-ttu-id="3645f-187">0x803C</span><span class="sxs-lookup"><span data-stu-id="3645f-187">0x803C</span></span>                          |
| <span data-ttu-id="3645f-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="3645f-188">System-Only</span></span>            | <span data-ttu-id="3645f-189">True</span><span class="sxs-lookup"><span data-stu-id="3645f-189">True</span></span>                            |
| <span data-ttu-id="3645f-190">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3645f-190">Is-Single-Valued</span></span>       | <span data-ttu-id="3645f-191">True</span><span class="sxs-lookup"><span data-stu-id="3645f-191">True</span></span>                            |
| <span data-ttu-id="3645f-192">É indexado</span><span class="sxs-lookup"><span data-stu-id="3645f-192">Is Indexed</span></span>             | <span data-ttu-id="3645f-193">Falso</span><span class="sxs-lookup"><span data-stu-id="3645f-193">False</span></span>                           |
| <span data-ttu-id="3645f-194">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3645f-194">In Global Catalog</span></span>      | <span data-ttu-id="3645f-195">True</span><span class="sxs-lookup"><span data-stu-id="3645f-195">True</span></span>                            |
| <span data-ttu-id="3645f-196">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3645f-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="3645f-197">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3645f-197">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3645f-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3645f-198">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3645f-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3645f-199">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3645f-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3645f-200">Search-Flags</span></span>           | <span data-ttu-id="3645f-201">0x00000008</span><span class="sxs-lookup"><span data-stu-id="3645f-201">0x00000008</span></span>                      |
| <span data-ttu-id="3645f-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3645f-202">System-Flags</span></span>           | <span data-ttu-id="3645f-203">0x00000013</span><span class="sxs-lookup"><span data-stu-id="3645f-203">0x00000013</span></span>                      |
| <span data-ttu-id="3645f-204">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3645f-204">Classes used in</span></span>        | [<span data-ttu-id="3645f-205">**Início**</span><span class="sxs-lookup"><span data-stu-id="3645f-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3645f-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3645f-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3645f-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="3645f-207">Entry</span></span> | <span data-ttu-id="3645f-208">Valor</span><span class="sxs-lookup"><span data-stu-id="3645f-208">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3645f-209">ID do link</span><span class="sxs-lookup"><span data-stu-id="3645f-209">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3645f-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3645f-210">MAPI-Id</span></span>                | <span data-ttu-id="3645f-211">0x803C</span><span class="sxs-lookup"><span data-stu-id="3645f-211">0x803C</span></span>                          |
| <span data-ttu-id="3645f-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="3645f-212">System-Only</span></span>            | <span data-ttu-id="3645f-213">True</span><span class="sxs-lookup"><span data-stu-id="3645f-213">True</span></span>                            |
| <span data-ttu-id="3645f-214">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3645f-214">Is-Single-Valued</span></span>       | <span data-ttu-id="3645f-215">True</span><span class="sxs-lookup"><span data-stu-id="3645f-215">True</span></span>                            |
| <span data-ttu-id="3645f-216">É indexado</span><span class="sxs-lookup"><span data-stu-id="3645f-216">Is Indexed</span></span>             | <span data-ttu-id="3645f-217">Falso</span><span class="sxs-lookup"><span data-stu-id="3645f-217">False</span></span>                           |
| <span data-ttu-id="3645f-218">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3645f-218">In Global Catalog</span></span>      | <span data-ttu-id="3645f-219">True</span><span class="sxs-lookup"><span data-stu-id="3645f-219">True</span></span>                            |
| <span data-ttu-id="3645f-220">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3645f-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="3645f-221">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3645f-221">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3645f-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3645f-222">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3645f-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3645f-223">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3645f-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3645f-224">Search-Flags</span></span>           | <span data-ttu-id="3645f-225">0x00000008</span><span class="sxs-lookup"><span data-stu-id="3645f-225">0x00000008</span></span>                      |
| <span data-ttu-id="3645f-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3645f-226">System-Flags</span></span>           | <span data-ttu-id="3645f-227">0x00000013</span><span class="sxs-lookup"><span data-stu-id="3645f-227">0x00000013</span></span>                      |
| <span data-ttu-id="3645f-228">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3645f-228">Classes used in</span></span>        | [<span data-ttu-id="3645f-229">**Início**</span><span class="sxs-lookup"><span data-stu-id="3645f-229">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3645f-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3645f-230">Windows Server 2008</span></span>



| <span data-ttu-id="3645f-231">Entrada</span><span class="sxs-lookup"><span data-stu-id="3645f-231">Entry</span></span> | <span data-ttu-id="3645f-232">Valor</span><span class="sxs-lookup"><span data-stu-id="3645f-232">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3645f-233">ID do link</span><span class="sxs-lookup"><span data-stu-id="3645f-233">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3645f-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3645f-234">MAPI-Id</span></span>                | <span data-ttu-id="3645f-235">0x803C</span><span class="sxs-lookup"><span data-stu-id="3645f-235">0x803C</span></span>                          |
| <span data-ttu-id="3645f-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="3645f-236">System-Only</span></span>            | <span data-ttu-id="3645f-237">True</span><span class="sxs-lookup"><span data-stu-id="3645f-237">True</span></span>                            |
| <span data-ttu-id="3645f-238">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3645f-238">Is-Single-Valued</span></span>       | <span data-ttu-id="3645f-239">True</span><span class="sxs-lookup"><span data-stu-id="3645f-239">True</span></span>                            |
| <span data-ttu-id="3645f-240">É indexado</span><span class="sxs-lookup"><span data-stu-id="3645f-240">Is Indexed</span></span>             | <span data-ttu-id="3645f-241">Falso</span><span class="sxs-lookup"><span data-stu-id="3645f-241">False</span></span>                           |
| <span data-ttu-id="3645f-242">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3645f-242">In Global Catalog</span></span>      | <span data-ttu-id="3645f-243">True</span><span class="sxs-lookup"><span data-stu-id="3645f-243">True</span></span>                            |
| <span data-ttu-id="3645f-244">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3645f-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="3645f-245">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3645f-245">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3645f-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3645f-246">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3645f-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3645f-247">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3645f-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3645f-248">Search-Flags</span></span>           | <span data-ttu-id="3645f-249">0x00000008</span><span class="sxs-lookup"><span data-stu-id="3645f-249">0x00000008</span></span>                      |
| <span data-ttu-id="3645f-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3645f-250">System-Flags</span></span>           | <span data-ttu-id="3645f-251">0x00000013</span><span class="sxs-lookup"><span data-stu-id="3645f-251">0x00000013</span></span>                      |
| <span data-ttu-id="3645f-252">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3645f-252">Classes used in</span></span>        | [<span data-ttu-id="3645f-253">**Início**</span><span class="sxs-lookup"><span data-stu-id="3645f-253">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3645f-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3645f-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3645f-255">Entrada</span><span class="sxs-lookup"><span data-stu-id="3645f-255">Entry</span></span> | <span data-ttu-id="3645f-256">Valor</span><span class="sxs-lookup"><span data-stu-id="3645f-256">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3645f-257">ID do link</span><span class="sxs-lookup"><span data-stu-id="3645f-257">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3645f-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3645f-258">MAPI-Id</span></span>                | <span data-ttu-id="3645f-259">0x803C</span><span class="sxs-lookup"><span data-stu-id="3645f-259">0x803C</span></span>                          |
| <span data-ttu-id="3645f-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="3645f-260">System-Only</span></span>            | <span data-ttu-id="3645f-261">True</span><span class="sxs-lookup"><span data-stu-id="3645f-261">True</span></span>                            |
| <span data-ttu-id="3645f-262">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3645f-262">Is-Single-Valued</span></span>       | <span data-ttu-id="3645f-263">True</span><span class="sxs-lookup"><span data-stu-id="3645f-263">True</span></span>                            |
| <span data-ttu-id="3645f-264">É indexado</span><span class="sxs-lookup"><span data-stu-id="3645f-264">Is Indexed</span></span>             | <span data-ttu-id="3645f-265">Falso</span><span class="sxs-lookup"><span data-stu-id="3645f-265">False</span></span>                           |
| <span data-ttu-id="3645f-266">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3645f-266">In Global Catalog</span></span>      | <span data-ttu-id="3645f-267">True</span><span class="sxs-lookup"><span data-stu-id="3645f-267">True</span></span>                            |
| <span data-ttu-id="3645f-268">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3645f-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="3645f-269">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3645f-269">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3645f-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3645f-270">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3645f-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3645f-271">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3645f-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3645f-272">Search-Flags</span></span>           | <span data-ttu-id="3645f-273">0x00000008</span><span class="sxs-lookup"><span data-stu-id="3645f-273">0x00000008</span></span>                      |
| <span data-ttu-id="3645f-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3645f-274">System-Flags</span></span>           | <span data-ttu-id="3645f-275">0x00000013</span><span class="sxs-lookup"><span data-stu-id="3645f-275">0x00000013</span></span>                      |
| <span data-ttu-id="3645f-276">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3645f-276">Classes used in</span></span>        | [<span data-ttu-id="3645f-277">**Início**</span><span class="sxs-lookup"><span data-stu-id="3645f-277">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3645f-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3645f-278">Windows Server 2012</span></span>



| <span data-ttu-id="3645f-279">Entrada</span><span class="sxs-lookup"><span data-stu-id="3645f-279">Entry</span></span> | <span data-ttu-id="3645f-280">Valor</span><span class="sxs-lookup"><span data-stu-id="3645f-280">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="3645f-281">ID do link</span><span class="sxs-lookup"><span data-stu-id="3645f-281">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="3645f-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3645f-282">MAPI-Id</span></span>                | <span data-ttu-id="3645f-283">0x803C</span><span class="sxs-lookup"><span data-stu-id="3645f-283">0x803C</span></span>                          |
| <span data-ttu-id="3645f-284">System-Only</span><span class="sxs-lookup"><span data-stu-id="3645f-284">System-Only</span></span>            | <span data-ttu-id="3645f-285">True</span><span class="sxs-lookup"><span data-stu-id="3645f-285">True</span></span>                            |
| <span data-ttu-id="3645f-286">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3645f-286">Is-Single-Valued</span></span>       | <span data-ttu-id="3645f-287">True</span><span class="sxs-lookup"><span data-stu-id="3645f-287">True</span></span>                            |
| <span data-ttu-id="3645f-288">É indexado</span><span class="sxs-lookup"><span data-stu-id="3645f-288">Is Indexed</span></span>             | <span data-ttu-id="3645f-289">Falso</span><span class="sxs-lookup"><span data-stu-id="3645f-289">False</span></span>                           |
| <span data-ttu-id="3645f-290">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3645f-290">In Global Catalog</span></span>      | <span data-ttu-id="3645f-291">True</span><span class="sxs-lookup"><span data-stu-id="3645f-291">True</span></span>                            |
| <span data-ttu-id="3645f-292">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3645f-292">NT-Security-Descriptor</span></span> | <span data-ttu-id="3645f-293">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3645f-293">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="3645f-294">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3645f-294">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="3645f-295">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3645f-295">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="3645f-296">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3645f-296">Search-Flags</span></span>           | <span data-ttu-id="3645f-297">0x00000008</span><span class="sxs-lookup"><span data-stu-id="3645f-297">0x00000008</span></span>                      |
| <span data-ttu-id="3645f-298">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3645f-298">System-Flags</span></span>           | <span data-ttu-id="3645f-299">0x00000013</span><span class="sxs-lookup"><span data-stu-id="3645f-299">0x00000013</span></span>                      |
| <span data-ttu-id="3645f-300">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3645f-300">Classes used in</span></span>        | [<span data-ttu-id="3645f-301">**Início**</span><span class="sxs-lookup"><span data-stu-id="3645f-301">**Top**</span></span>](c-top.md)<br/> |



 

 





