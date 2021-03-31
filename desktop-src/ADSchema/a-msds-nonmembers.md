---
title: atributo ms-DS-non-members
description: Esse atributo tem a mesma finalidade que o atributo de não-segurança-membro, mas com regras de escopo aplicadas.
ms.assetid: 11d3d030-3643-4ed2-a52e-a57f32e9597f
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo ms-DS-non-members
- atributo msDS-não membros do AD Schema
topic_type:
- apiref
api_name:
- ms-DS-Non-Members
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca8ca19af90f2f534f974863aa7d766f6be4624b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825198"
---
# <a name="ms-ds-non-members-attribute"></a><span data-ttu-id="86cde-105">atributo ms-DS-non-members</span><span class="sxs-lookup"><span data-stu-id="86cde-105">ms-DS-Non-Members attribute</span></span>

<span data-ttu-id="86cde-106">Esse atributo tem a mesma finalidade que o atributo de não-segurança-membro, mas com regras de escopo aplicadas.</span><span class="sxs-lookup"><span data-stu-id="86cde-106">This attribute serves the same purpose as the Non-Security-Member attribute but with scoping rules applied.</span></span>



| <span data-ttu-id="86cde-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="86cde-107">Entry</span></span> | <span data-ttu-id="86cde-108">Valor</span><span class="sxs-lookup"><span data-stu-id="86cde-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="86cde-109">CN</span><span class="sxs-lookup"><span data-stu-id="86cde-109">CN</span></span>                | <span data-ttu-id="86cde-110">ms-DS-não-membros</span><span class="sxs-lookup"><span data-stu-id="86cde-110">ms-DS-Non-Members</span></span>                       |
| <span data-ttu-id="86cde-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="86cde-111">Ldap-Display-Name</span></span> | <span data-ttu-id="86cde-112">msDS-não membros</span><span class="sxs-lookup"><span data-stu-id="86cde-112">msDS-NonMembers</span></span>                         |
| <span data-ttu-id="86cde-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="86cde-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="86cde-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="86cde-114">Update Privilege</span></span>  | <span data-ttu-id="86cde-115">Administrador do AzRoles</span><span class="sxs-lookup"><span data-stu-id="86cde-115">AzRoles Admin</span></span>                           |
| <span data-ttu-id="86cde-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="86cde-116">Update Frequency</span></span>  | <span data-ttu-id="86cde-117">Na inicialização e na alteração da política.</span><span class="sxs-lookup"><span data-stu-id="86cde-117">At initialization and policy change.</span></span>    |
| <span data-ttu-id="86cde-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="86cde-118">Attribute-Id</span></span>      | <span data-ttu-id="86cde-119">1.2.840.113556.1.4.1793</span><span class="sxs-lookup"><span data-stu-id="86cde-119">1.2.840.113556.1.4.1793</span></span>                 |
| <span data-ttu-id="86cde-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="86cde-120">System-Id-Guid</span></span>    | <span data-ttu-id="86cde-121">cafcb1de-f23c-46b5-adf7-1e64957bd5db</span><span class="sxs-lookup"><span data-stu-id="86cde-121">cafcb1de-f23c-46b5-adf7-1e64957bd5db</span></span>    |
| <span data-ttu-id="86cde-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="86cde-122">Syntax</span></span>            | [<span data-ttu-id="86cde-123">**Objeto (DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="86cde-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="86cde-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="86cde-124">Implementations</span></span>

-   [<span data-ttu-id="86cde-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="86cde-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="86cde-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="86cde-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="86cde-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="86cde-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="86cde-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="86cde-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="86cde-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="86cde-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="86cde-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="86cde-130">Windows Server 2003</span></span>



| <span data-ttu-id="86cde-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="86cde-131">Entry</span></span> | <span data-ttu-id="86cde-132">Valor</span><span class="sxs-lookup"><span data-stu-id="86cde-132">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="86cde-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="86cde-133">Link-Id</span></span>                | <span data-ttu-id="86cde-134">2014</span><span class="sxs-lookup"><span data-stu-id="86cde-134">2014</span></span>                                |
| <span data-ttu-id="86cde-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="86cde-135">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="86cde-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="86cde-136">System-Only</span></span>            | <span data-ttu-id="86cde-137">Falso</span><span class="sxs-lookup"><span data-stu-id="86cde-137">False</span></span>                               |
| <span data-ttu-id="86cde-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="86cde-138">Is-Single-Valued</span></span>       | <span data-ttu-id="86cde-139">Falso</span><span class="sxs-lookup"><span data-stu-id="86cde-139">False</span></span>                               |
| <span data-ttu-id="86cde-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="86cde-140">Is Indexed</span></span>             | <span data-ttu-id="86cde-141">Falso</span><span class="sxs-lookup"><span data-stu-id="86cde-141">False</span></span>                               |
| <span data-ttu-id="86cde-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="86cde-142">In Global Catalog</span></span>      | <span data-ttu-id="86cde-143">Falso</span><span class="sxs-lookup"><span data-stu-id="86cde-143">False</span></span>                               |
| <span data-ttu-id="86cde-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="86cde-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="86cde-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="86cde-145">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="86cde-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="86cde-146">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="86cde-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="86cde-147">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="86cde-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="86cde-148">Search-Flags</span></span>           | <span data-ttu-id="86cde-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="86cde-149">0x00000000</span></span>                          |
| <span data-ttu-id="86cde-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="86cde-150">System-Flags</span></span>           | <span data-ttu-id="86cde-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="86cde-151">0x00000010</span></span>                          |
| <span data-ttu-id="86cde-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="86cde-152">Classes used in</span></span>        | [<span data-ttu-id="86cde-153">**Group**</span><span class="sxs-lookup"><span data-stu-id="86cde-153">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="86cde-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="86cde-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="86cde-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="86cde-155">Entry</span></span> | <span data-ttu-id="86cde-156">Valor</span><span class="sxs-lookup"><span data-stu-id="86cde-156">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="86cde-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="86cde-157">Link-Id</span></span>                | <span data-ttu-id="86cde-158">2014</span><span class="sxs-lookup"><span data-stu-id="86cde-158">2014</span></span>                                |
| <span data-ttu-id="86cde-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="86cde-159">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="86cde-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="86cde-160">System-Only</span></span>            | <span data-ttu-id="86cde-161">Falso</span><span class="sxs-lookup"><span data-stu-id="86cde-161">False</span></span>                               |
| <span data-ttu-id="86cde-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="86cde-162">Is-Single-Valued</span></span>       | <span data-ttu-id="86cde-163">Falso</span><span class="sxs-lookup"><span data-stu-id="86cde-163">False</span></span>                               |
| <span data-ttu-id="86cde-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="86cde-164">Is Indexed</span></span>             | <span data-ttu-id="86cde-165">Falso</span><span class="sxs-lookup"><span data-stu-id="86cde-165">False</span></span>                               |
| <span data-ttu-id="86cde-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="86cde-166">In Global Catalog</span></span>      | <span data-ttu-id="86cde-167">Falso</span><span class="sxs-lookup"><span data-stu-id="86cde-167">False</span></span>                               |
| <span data-ttu-id="86cde-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="86cde-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="86cde-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="86cde-169">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="86cde-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="86cde-170">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="86cde-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="86cde-171">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="86cde-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="86cde-172">Search-Flags</span></span>           | <span data-ttu-id="86cde-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="86cde-173">0x00000000</span></span>                          |
| <span data-ttu-id="86cde-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="86cde-174">System-Flags</span></span>           | <span data-ttu-id="86cde-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="86cde-175">0x00000010</span></span>                          |
| <span data-ttu-id="86cde-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="86cde-176">Classes used in</span></span>        | [<span data-ttu-id="86cde-177">**Group**</span><span class="sxs-lookup"><span data-stu-id="86cde-177">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="86cde-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="86cde-178">Windows Server 2008</span></span>



| <span data-ttu-id="86cde-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="86cde-179">Entry</span></span> | <span data-ttu-id="86cde-180">Valor</span><span class="sxs-lookup"><span data-stu-id="86cde-180">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="86cde-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="86cde-181">Link-Id</span></span>                | <span data-ttu-id="86cde-182">2014</span><span class="sxs-lookup"><span data-stu-id="86cde-182">2014</span></span>                                |
| <span data-ttu-id="86cde-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="86cde-183">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="86cde-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="86cde-184">System-Only</span></span>            | <span data-ttu-id="86cde-185">Falso</span><span class="sxs-lookup"><span data-stu-id="86cde-185">False</span></span>                               |
| <span data-ttu-id="86cde-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="86cde-186">Is-Single-Valued</span></span>       | <span data-ttu-id="86cde-187">Falso</span><span class="sxs-lookup"><span data-stu-id="86cde-187">False</span></span>                               |
| <span data-ttu-id="86cde-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="86cde-188">Is Indexed</span></span>             | <span data-ttu-id="86cde-189">Falso</span><span class="sxs-lookup"><span data-stu-id="86cde-189">False</span></span>                               |
| <span data-ttu-id="86cde-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="86cde-190">In Global Catalog</span></span>      | <span data-ttu-id="86cde-191">Falso</span><span class="sxs-lookup"><span data-stu-id="86cde-191">False</span></span>                               |
| <span data-ttu-id="86cde-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="86cde-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="86cde-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="86cde-193">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="86cde-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="86cde-194">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="86cde-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="86cde-195">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="86cde-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="86cde-196">Search-Flags</span></span>           | <span data-ttu-id="86cde-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="86cde-197">0x00000000</span></span>                          |
| <span data-ttu-id="86cde-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="86cde-198">System-Flags</span></span>           | <span data-ttu-id="86cde-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="86cde-199">0x00000010</span></span>                          |
| <span data-ttu-id="86cde-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="86cde-200">Classes used in</span></span>        | [<span data-ttu-id="86cde-201">**Group**</span><span class="sxs-lookup"><span data-stu-id="86cde-201">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="86cde-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="86cde-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="86cde-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="86cde-203">Entry</span></span> | <span data-ttu-id="86cde-204">Valor</span><span class="sxs-lookup"><span data-stu-id="86cde-204">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="86cde-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="86cde-205">Link-Id</span></span>                | <span data-ttu-id="86cde-206">2014</span><span class="sxs-lookup"><span data-stu-id="86cde-206">2014</span></span>                                |
| <span data-ttu-id="86cde-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="86cde-207">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="86cde-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="86cde-208">System-Only</span></span>            | <span data-ttu-id="86cde-209">Falso</span><span class="sxs-lookup"><span data-stu-id="86cde-209">False</span></span>                               |
| <span data-ttu-id="86cde-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="86cde-210">Is-Single-Valued</span></span>       | <span data-ttu-id="86cde-211">Falso</span><span class="sxs-lookup"><span data-stu-id="86cde-211">False</span></span>                               |
| <span data-ttu-id="86cde-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="86cde-212">Is Indexed</span></span>             | <span data-ttu-id="86cde-213">Falso</span><span class="sxs-lookup"><span data-stu-id="86cde-213">False</span></span>                               |
| <span data-ttu-id="86cde-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="86cde-214">In Global Catalog</span></span>      | <span data-ttu-id="86cde-215">Falso</span><span class="sxs-lookup"><span data-stu-id="86cde-215">False</span></span>                               |
| <span data-ttu-id="86cde-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="86cde-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="86cde-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="86cde-217">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="86cde-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="86cde-218">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="86cde-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="86cde-219">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="86cde-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="86cde-220">Search-Flags</span></span>           | <span data-ttu-id="86cde-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="86cde-221">0x00000000</span></span>                          |
| <span data-ttu-id="86cde-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="86cde-222">System-Flags</span></span>           | <span data-ttu-id="86cde-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="86cde-223">0x00000010</span></span>                          |
| <span data-ttu-id="86cde-224">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="86cde-224">Classes used in</span></span>        | [<span data-ttu-id="86cde-225">**Group**</span><span class="sxs-lookup"><span data-stu-id="86cde-225">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="86cde-226">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="86cde-226">Windows Server 2012</span></span>



| <span data-ttu-id="86cde-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="86cde-227">Entry</span></span> | <span data-ttu-id="86cde-228">Valor</span><span class="sxs-lookup"><span data-stu-id="86cde-228">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="86cde-229">ID do link</span><span class="sxs-lookup"><span data-stu-id="86cde-229">Link-Id</span></span>                | <span data-ttu-id="86cde-230">2014</span><span class="sxs-lookup"><span data-stu-id="86cde-230">2014</span></span>                                |
| <span data-ttu-id="86cde-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="86cde-231">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="86cde-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="86cde-232">System-Only</span></span>            | <span data-ttu-id="86cde-233">Falso</span><span class="sxs-lookup"><span data-stu-id="86cde-233">False</span></span>                               |
| <span data-ttu-id="86cde-234">É de valor único</span><span class="sxs-lookup"><span data-stu-id="86cde-234">Is-Single-Valued</span></span>       | <span data-ttu-id="86cde-235">Falso</span><span class="sxs-lookup"><span data-stu-id="86cde-235">False</span></span>                               |
| <span data-ttu-id="86cde-236">É indexado</span><span class="sxs-lookup"><span data-stu-id="86cde-236">Is Indexed</span></span>             | <span data-ttu-id="86cde-237">Falso</span><span class="sxs-lookup"><span data-stu-id="86cde-237">False</span></span>                               |
| <span data-ttu-id="86cde-238">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="86cde-238">In Global Catalog</span></span>      | <span data-ttu-id="86cde-239">Falso</span><span class="sxs-lookup"><span data-stu-id="86cde-239">False</span></span>                               |
| <span data-ttu-id="86cde-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="86cde-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="86cde-241">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="86cde-241">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="86cde-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="86cde-242">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="86cde-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="86cde-243">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="86cde-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="86cde-244">Search-Flags</span></span>           | <span data-ttu-id="86cde-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="86cde-245">0x00000000</span></span>                          |
| <span data-ttu-id="86cde-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="86cde-246">System-Flags</span></span>           | <span data-ttu-id="86cde-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="86cde-247">0x00000010</span></span>                          |
| <span data-ttu-id="86cde-248">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="86cde-248">Classes used in</span></span>        | [<span data-ttu-id="86cde-249">**Group**</span><span class="sxs-lookup"><span data-stu-id="86cde-249">**Group**</span></span>](c-group.md)<br/> |



 

 





