---
title: Is-Deleted atributo
description: Se for TRUE, esse objeto foi marcado para exclusão e não poderá ser instanciado. Depois que o período de marca para exclusão tiver expirado, ele será removido do sistema.
ms.assetid: 549b5161-5d2f-47d7-8192-4480334ef13d
ms.tgt_platform: multiple
keywords:
- Esquema de Is-Deleted do atributo AD
- Esquema de AD do atributo isDeleted
topic_type:
- apiref
api_name:
- Is-Deleted
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b30dec5ed139da60853324b82cc6e0f55fcc70
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105762787"
---
# <a name="is-deleted-attribute"></a><span data-ttu-id="be59f-106">Is-Deleted atributo</span><span class="sxs-lookup"><span data-stu-id="be59f-106">Is-Deleted attribute</span></span>

<span data-ttu-id="be59f-107">Se **for true**, esse objeto foi marcado para exclusão e não poderá ser instanciado.</span><span class="sxs-lookup"><span data-stu-id="be59f-107">If **TRUE**, this object has been marked for deletion and cannot be instantiated.</span></span> <span data-ttu-id="be59f-108">Depois que o período de marca para exclusão tiver expirado, ele será removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="be59f-108">After the tombstone period has expired, it will be removed from the system.</span></span>



| <span data-ttu-id="be59f-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="be59f-109">Entry</span></span> | <span data-ttu-id="be59f-110">Valor</span><span class="sxs-lookup"><span data-stu-id="be59f-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="be59f-111">CN</span><span class="sxs-lookup"><span data-stu-id="be59f-111">CN</span></span>                | <span data-ttu-id="be59f-112">Is-Deleted</span><span class="sxs-lookup"><span data-stu-id="be59f-112">Is-Deleted</span></span>                           |
| <span data-ttu-id="be59f-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="be59f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="be59f-114">isDeleted</span><span class="sxs-lookup"><span data-stu-id="be59f-114">isDeleted</span></span>                            |
| <span data-ttu-id="be59f-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="be59f-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="be59f-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="be59f-116">Update Privilege</span></span>  | <span data-ttu-id="be59f-117">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="be59f-117">Domain administrator</span></span>                 |
| <span data-ttu-id="be59f-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="be59f-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="be59f-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="be59f-119">Attribute-Id</span></span>      | <span data-ttu-id="be59f-120">1.2.840.113556.1.2.48</span><span class="sxs-lookup"><span data-stu-id="be59f-120">1.2.840.113556.1.2.48</span></span>                |
| <span data-ttu-id="be59f-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="be59f-121">System-Id-Guid</span></span>    | <span data-ttu-id="be59f-122">bf96798f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="be59f-122">bf96798f-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="be59f-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="be59f-123">Syntax</span></span>            | [<span data-ttu-id="be59f-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="be59f-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="be59f-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="be59f-125">Implementations</span></span>

-   [<span data-ttu-id="be59f-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="be59f-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="be59f-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="be59f-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="be59f-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="be59f-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="be59f-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="be59f-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="be59f-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="be59f-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="be59f-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="be59f-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="be59f-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="be59f-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="be59f-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="be59f-133">Windows 2000 Server</span></span>



| <span data-ttu-id="be59f-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="be59f-134">Entry</span></span> | <span data-ttu-id="be59f-135">Valor</span><span class="sxs-lookup"><span data-stu-id="be59f-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="be59f-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="be59f-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="be59f-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be59f-137">MAPI-Id</span></span>                | <span data-ttu-id="be59f-138">0x80C0</span><span class="sxs-lookup"><span data-stu-id="be59f-138">0x80C0</span></span>                          |
| <span data-ttu-id="be59f-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="be59f-139">System-Only</span></span>            | <span data-ttu-id="be59f-140">True</span><span class="sxs-lookup"><span data-stu-id="be59f-140">True</span></span>                            |
| <span data-ttu-id="be59f-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="be59f-141">Is-Single-Valued</span></span>       | <span data-ttu-id="be59f-142">True</span><span class="sxs-lookup"><span data-stu-id="be59f-142">True</span></span>                            |
| <span data-ttu-id="be59f-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="be59f-143">Is Indexed</span></span>             | <span data-ttu-id="be59f-144">Falso</span><span class="sxs-lookup"><span data-stu-id="be59f-144">False</span></span>                           |
| <span data-ttu-id="be59f-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="be59f-145">In Global Catalog</span></span>      | <span data-ttu-id="be59f-146">True</span><span class="sxs-lookup"><span data-stu-id="be59f-146">True</span></span>                            |
| <span data-ttu-id="be59f-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="be59f-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="be59f-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="be59f-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="be59f-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be59f-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="be59f-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be59f-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="be59f-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be59f-151">Search-Flags</span></span>           | <span data-ttu-id="be59f-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be59f-152">0x00000000</span></span>                      |
| <span data-ttu-id="be59f-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be59f-153">System-Flags</span></span>           | <span data-ttu-id="be59f-154">0x00000012</span><span class="sxs-lookup"><span data-stu-id="be59f-154">0x00000012</span></span>                      |
| <span data-ttu-id="be59f-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="be59f-155">Classes used in</span></span>        | [<span data-ttu-id="be59f-156">**Início**</span><span class="sxs-lookup"><span data-stu-id="be59f-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="be59f-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="be59f-157">Windows Server 2003</span></span>



| <span data-ttu-id="be59f-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="be59f-158">Entry</span></span> | <span data-ttu-id="be59f-159">Valor</span><span class="sxs-lookup"><span data-stu-id="be59f-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="be59f-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="be59f-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="be59f-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be59f-161">MAPI-Id</span></span>                | <span data-ttu-id="be59f-162">0x80C0</span><span class="sxs-lookup"><span data-stu-id="be59f-162">0x80C0</span></span>                          |
| <span data-ttu-id="be59f-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="be59f-163">System-Only</span></span>            | <span data-ttu-id="be59f-164">True</span><span class="sxs-lookup"><span data-stu-id="be59f-164">True</span></span>                            |
| <span data-ttu-id="be59f-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="be59f-165">Is-Single-Valued</span></span>       | <span data-ttu-id="be59f-166">True</span><span class="sxs-lookup"><span data-stu-id="be59f-166">True</span></span>                            |
| <span data-ttu-id="be59f-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="be59f-167">Is Indexed</span></span>             | <span data-ttu-id="be59f-168">Falso</span><span class="sxs-lookup"><span data-stu-id="be59f-168">False</span></span>                           |
| <span data-ttu-id="be59f-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="be59f-169">In Global Catalog</span></span>      | <span data-ttu-id="be59f-170">True</span><span class="sxs-lookup"><span data-stu-id="be59f-170">True</span></span>                            |
| <span data-ttu-id="be59f-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="be59f-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="be59f-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="be59f-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="be59f-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be59f-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="be59f-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be59f-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="be59f-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be59f-175">Search-Flags</span></span>           | <span data-ttu-id="be59f-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be59f-176">0x00000000</span></span>                      |
| <span data-ttu-id="be59f-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be59f-177">System-Flags</span></span>           | <span data-ttu-id="be59f-178">0x00000012</span><span class="sxs-lookup"><span data-stu-id="be59f-178">0x00000012</span></span>                      |
| <span data-ttu-id="be59f-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="be59f-179">Classes used in</span></span>        | [<span data-ttu-id="be59f-180">**Início**</span><span class="sxs-lookup"><span data-stu-id="be59f-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="be59f-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="be59f-181">ADAM</span></span>



| <span data-ttu-id="be59f-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="be59f-182">Entry</span></span> | <span data-ttu-id="be59f-183">Valor</span><span class="sxs-lookup"><span data-stu-id="be59f-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="be59f-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="be59f-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="be59f-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be59f-185">MAPI-Id</span></span>                | <span data-ttu-id="be59f-186">0x80C0</span><span class="sxs-lookup"><span data-stu-id="be59f-186">0x80C0</span></span>                          |
| <span data-ttu-id="be59f-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="be59f-187">System-Only</span></span>            | <span data-ttu-id="be59f-188">True</span><span class="sxs-lookup"><span data-stu-id="be59f-188">True</span></span>                            |
| <span data-ttu-id="be59f-189">É de valor único</span><span class="sxs-lookup"><span data-stu-id="be59f-189">Is-Single-Valued</span></span>       | <span data-ttu-id="be59f-190">True</span><span class="sxs-lookup"><span data-stu-id="be59f-190">True</span></span>                            |
| <span data-ttu-id="be59f-191">É indexado</span><span class="sxs-lookup"><span data-stu-id="be59f-191">Is Indexed</span></span>             | <span data-ttu-id="be59f-192">Falso</span><span class="sxs-lookup"><span data-stu-id="be59f-192">False</span></span>                           |
| <span data-ttu-id="be59f-193">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="be59f-193">In Global Catalog</span></span>      | <span data-ttu-id="be59f-194">True</span><span class="sxs-lookup"><span data-stu-id="be59f-194">True</span></span>                            |
| <span data-ttu-id="be59f-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="be59f-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="be59f-196">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="be59f-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="be59f-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be59f-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="be59f-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be59f-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="be59f-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be59f-199">Search-Flags</span></span>           | <span data-ttu-id="be59f-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be59f-200">0x00000000</span></span>                      |
| <span data-ttu-id="be59f-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be59f-201">System-Flags</span></span>           | <span data-ttu-id="be59f-202">0x00000012</span><span class="sxs-lookup"><span data-stu-id="be59f-202">0x00000012</span></span>                      |
| <span data-ttu-id="be59f-203">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="be59f-203">Classes used in</span></span>        | [<span data-ttu-id="be59f-204">**Início**</span><span class="sxs-lookup"><span data-stu-id="be59f-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="be59f-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="be59f-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="be59f-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="be59f-206">Entry</span></span> | <span data-ttu-id="be59f-207">Valor</span><span class="sxs-lookup"><span data-stu-id="be59f-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="be59f-208">ID do link</span><span class="sxs-lookup"><span data-stu-id="be59f-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="be59f-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be59f-209">MAPI-Id</span></span>                | <span data-ttu-id="be59f-210">0x80C0</span><span class="sxs-lookup"><span data-stu-id="be59f-210">0x80C0</span></span>                          |
| <span data-ttu-id="be59f-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="be59f-211">System-Only</span></span>            | <span data-ttu-id="be59f-212">True</span><span class="sxs-lookup"><span data-stu-id="be59f-212">True</span></span>                            |
| <span data-ttu-id="be59f-213">É de valor único</span><span class="sxs-lookup"><span data-stu-id="be59f-213">Is-Single-Valued</span></span>       | <span data-ttu-id="be59f-214">True</span><span class="sxs-lookup"><span data-stu-id="be59f-214">True</span></span>                            |
| <span data-ttu-id="be59f-215">É indexado</span><span class="sxs-lookup"><span data-stu-id="be59f-215">Is Indexed</span></span>             | <span data-ttu-id="be59f-216">Falso</span><span class="sxs-lookup"><span data-stu-id="be59f-216">False</span></span>                           |
| <span data-ttu-id="be59f-217">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="be59f-217">In Global Catalog</span></span>      | <span data-ttu-id="be59f-218">True</span><span class="sxs-lookup"><span data-stu-id="be59f-218">True</span></span>                            |
| <span data-ttu-id="be59f-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="be59f-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="be59f-220">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="be59f-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="be59f-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be59f-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="be59f-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be59f-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="be59f-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be59f-223">Search-Flags</span></span>           | <span data-ttu-id="be59f-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be59f-224">0x00000000</span></span>                      |
| <span data-ttu-id="be59f-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be59f-225">System-Flags</span></span>           | <span data-ttu-id="be59f-226">0x00000012</span><span class="sxs-lookup"><span data-stu-id="be59f-226">0x00000012</span></span>                      |
| <span data-ttu-id="be59f-227">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="be59f-227">Classes used in</span></span>        | [<span data-ttu-id="be59f-228">**Início**</span><span class="sxs-lookup"><span data-stu-id="be59f-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="be59f-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be59f-229">Windows Server 2008</span></span>



| <span data-ttu-id="be59f-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="be59f-230">Entry</span></span> | <span data-ttu-id="be59f-231">Valor</span><span class="sxs-lookup"><span data-stu-id="be59f-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="be59f-232">ID do link</span><span class="sxs-lookup"><span data-stu-id="be59f-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="be59f-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be59f-233">MAPI-Id</span></span>                | <span data-ttu-id="be59f-234">0x80C0</span><span class="sxs-lookup"><span data-stu-id="be59f-234">0x80C0</span></span>                          |
| <span data-ttu-id="be59f-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="be59f-235">System-Only</span></span>            | <span data-ttu-id="be59f-236">True</span><span class="sxs-lookup"><span data-stu-id="be59f-236">True</span></span>                            |
| <span data-ttu-id="be59f-237">É de valor único</span><span class="sxs-lookup"><span data-stu-id="be59f-237">Is-Single-Valued</span></span>       | <span data-ttu-id="be59f-238">True</span><span class="sxs-lookup"><span data-stu-id="be59f-238">True</span></span>                            |
| <span data-ttu-id="be59f-239">É indexado</span><span class="sxs-lookup"><span data-stu-id="be59f-239">Is Indexed</span></span>             | <span data-ttu-id="be59f-240">Falso</span><span class="sxs-lookup"><span data-stu-id="be59f-240">False</span></span>                           |
| <span data-ttu-id="be59f-241">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="be59f-241">In Global Catalog</span></span>      | <span data-ttu-id="be59f-242">True</span><span class="sxs-lookup"><span data-stu-id="be59f-242">True</span></span>                            |
| <span data-ttu-id="be59f-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="be59f-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="be59f-244">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="be59f-244">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="be59f-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be59f-245">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="be59f-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be59f-246">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="be59f-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be59f-247">Search-Flags</span></span>           | <span data-ttu-id="be59f-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be59f-248">0x00000000</span></span>                      |
| <span data-ttu-id="be59f-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be59f-249">System-Flags</span></span>           | <span data-ttu-id="be59f-250">0x00000012</span><span class="sxs-lookup"><span data-stu-id="be59f-250">0x00000012</span></span>                      |
| <span data-ttu-id="be59f-251">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="be59f-251">Classes used in</span></span>        | [<span data-ttu-id="be59f-252">**Início**</span><span class="sxs-lookup"><span data-stu-id="be59f-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="be59f-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="be59f-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="be59f-254">Entrada</span><span class="sxs-lookup"><span data-stu-id="be59f-254">Entry</span></span> | <span data-ttu-id="be59f-255">Valor</span><span class="sxs-lookup"><span data-stu-id="be59f-255">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="be59f-256">ID do link</span><span class="sxs-lookup"><span data-stu-id="be59f-256">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="be59f-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be59f-257">MAPI-Id</span></span>                | <span data-ttu-id="be59f-258">0x80C0</span><span class="sxs-lookup"><span data-stu-id="be59f-258">0x80C0</span></span>                          |
| <span data-ttu-id="be59f-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="be59f-259">System-Only</span></span>            | <span data-ttu-id="be59f-260">True</span><span class="sxs-lookup"><span data-stu-id="be59f-260">True</span></span>                            |
| <span data-ttu-id="be59f-261">É de valor único</span><span class="sxs-lookup"><span data-stu-id="be59f-261">Is-Single-Valued</span></span>       | <span data-ttu-id="be59f-262">True</span><span class="sxs-lookup"><span data-stu-id="be59f-262">True</span></span>                            |
| <span data-ttu-id="be59f-263">É indexado</span><span class="sxs-lookup"><span data-stu-id="be59f-263">Is Indexed</span></span>             | <span data-ttu-id="be59f-264">Falso</span><span class="sxs-lookup"><span data-stu-id="be59f-264">False</span></span>                           |
| <span data-ttu-id="be59f-265">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="be59f-265">In Global Catalog</span></span>      | <span data-ttu-id="be59f-266">True</span><span class="sxs-lookup"><span data-stu-id="be59f-266">True</span></span>                            |
| <span data-ttu-id="be59f-267">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="be59f-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="be59f-268">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="be59f-268">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="be59f-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be59f-269">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="be59f-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be59f-270">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="be59f-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be59f-271">Search-Flags</span></span>           | <span data-ttu-id="be59f-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be59f-272">0x00000000</span></span>                      |
| <span data-ttu-id="be59f-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be59f-273">System-Flags</span></span>           | <span data-ttu-id="be59f-274">0x00000012</span><span class="sxs-lookup"><span data-stu-id="be59f-274">0x00000012</span></span>                      |
| <span data-ttu-id="be59f-275">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="be59f-275">Classes used in</span></span>        | [<span data-ttu-id="be59f-276">**Início**</span><span class="sxs-lookup"><span data-stu-id="be59f-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="be59f-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="be59f-277">Windows Server 2012</span></span>



| <span data-ttu-id="be59f-278">Entrada</span><span class="sxs-lookup"><span data-stu-id="be59f-278">Entry</span></span> | <span data-ttu-id="be59f-279">Valor</span><span class="sxs-lookup"><span data-stu-id="be59f-279">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="be59f-280">ID do link</span><span class="sxs-lookup"><span data-stu-id="be59f-280">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="be59f-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="be59f-281">MAPI-Id</span></span>                | <span data-ttu-id="be59f-282">0x80C0</span><span class="sxs-lookup"><span data-stu-id="be59f-282">0x80C0</span></span>                          |
| <span data-ttu-id="be59f-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="be59f-283">System-Only</span></span>            | <span data-ttu-id="be59f-284">True</span><span class="sxs-lookup"><span data-stu-id="be59f-284">True</span></span>                            |
| <span data-ttu-id="be59f-285">É de valor único</span><span class="sxs-lookup"><span data-stu-id="be59f-285">Is-Single-Valued</span></span>       | <span data-ttu-id="be59f-286">True</span><span class="sxs-lookup"><span data-stu-id="be59f-286">True</span></span>                            |
| <span data-ttu-id="be59f-287">É indexado</span><span class="sxs-lookup"><span data-stu-id="be59f-287">Is Indexed</span></span>             | <span data-ttu-id="be59f-288">Falso</span><span class="sxs-lookup"><span data-stu-id="be59f-288">False</span></span>                           |
| <span data-ttu-id="be59f-289">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="be59f-289">In Global Catalog</span></span>      | <span data-ttu-id="be59f-290">True</span><span class="sxs-lookup"><span data-stu-id="be59f-290">True</span></span>                            |
| <span data-ttu-id="be59f-291">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="be59f-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="be59f-292">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="be59f-292">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="be59f-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="be59f-293">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="be59f-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="be59f-294">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="be59f-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="be59f-295">Search-Flags</span></span>           | <span data-ttu-id="be59f-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="be59f-296">0x00000000</span></span>                      |
| <span data-ttu-id="be59f-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="be59f-297">System-Flags</span></span>           | <span data-ttu-id="be59f-298">0x00000012</span><span class="sxs-lookup"><span data-stu-id="be59f-298">0x00000012</span></span>                      |
| <span data-ttu-id="be59f-299">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="be59f-299">Classes used in</span></span>        | [<span data-ttu-id="be59f-300">**Início**</span><span class="sxs-lookup"><span data-stu-id="be59f-300">**Top**</span></span>](c-top.md)<br/> |



 

 





