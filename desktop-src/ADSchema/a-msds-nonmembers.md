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
# <a name="ms-ds-non-members-attribute"></a><span data-ttu-id="d1b71-105">atributo ms-DS-non-members</span><span class="sxs-lookup"><span data-stu-id="d1b71-105">ms-DS-Non-Members attribute</span></span>

<span data-ttu-id="d1b71-106">Esse atributo tem a mesma finalidade que o atributo de não-segurança-membro, mas com regras de escopo aplicadas.</span><span class="sxs-lookup"><span data-stu-id="d1b71-106">This attribute serves the same purpose as the Non-Security-Member attribute but with scoping rules applied.</span></span>



| <span data-ttu-id="d1b71-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="d1b71-107">Entry</span></span> | <span data-ttu-id="d1b71-108">Valor</span><span class="sxs-lookup"><span data-stu-id="d1b71-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="d1b71-109">CN</span><span class="sxs-lookup"><span data-stu-id="d1b71-109">CN</span></span>                | <span data-ttu-id="d1b71-110">ms-DS-não-membros</span><span class="sxs-lookup"><span data-stu-id="d1b71-110">ms-DS-Non-Members</span></span>                       |
| <span data-ttu-id="d1b71-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d1b71-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d1b71-112">msDS-não membros</span><span class="sxs-lookup"><span data-stu-id="d1b71-112">msDS-NonMembers</span></span>                         |
| <span data-ttu-id="d1b71-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="d1b71-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="d1b71-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="d1b71-114">Update Privilege</span></span>  | <span data-ttu-id="d1b71-115">Administrador do AzRoles</span><span class="sxs-lookup"><span data-stu-id="d1b71-115">AzRoles Admin</span></span>                           |
| <span data-ttu-id="d1b71-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="d1b71-116">Update Frequency</span></span>  | <span data-ttu-id="d1b71-117">Na inicialização e na alteração da política.</span><span class="sxs-lookup"><span data-stu-id="d1b71-117">At initialization and policy change.</span></span>    |
| <span data-ttu-id="d1b71-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d1b71-118">Attribute-Id</span></span>      | <span data-ttu-id="d1b71-119">1.2.840.113556.1.4.1793</span><span class="sxs-lookup"><span data-stu-id="d1b71-119">1.2.840.113556.1.4.1793</span></span>                 |
| <span data-ttu-id="d1b71-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d1b71-120">System-Id-Guid</span></span>    | <span data-ttu-id="d1b71-121">cafcb1de-f23c-46b5-adf7-1e64957bd5db</span><span class="sxs-lookup"><span data-stu-id="d1b71-121">cafcb1de-f23c-46b5-adf7-1e64957bd5db</span></span>    |
| <span data-ttu-id="d1b71-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1b71-122">Syntax</span></span>            | [<span data-ttu-id="d1b71-123">**Objeto (DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="d1b71-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="d1b71-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="d1b71-124">Implementations</span></span>

-   [<span data-ttu-id="d1b71-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d1b71-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d1b71-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d1b71-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d1b71-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d1b71-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d1b71-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d1b71-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d1b71-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d1b71-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="d1b71-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d1b71-130">Windows Server 2003</span></span>



| <span data-ttu-id="d1b71-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="d1b71-131">Entry</span></span> | <span data-ttu-id="d1b71-132">Valor</span><span class="sxs-lookup"><span data-stu-id="d1b71-132">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="d1b71-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="d1b71-133">Link-Id</span></span>                | <span data-ttu-id="d1b71-134">2014</span><span class="sxs-lookup"><span data-stu-id="d1b71-134">2014</span></span>                                |
| <span data-ttu-id="d1b71-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1b71-135">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="d1b71-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1b71-136">System-Only</span></span>            | <span data-ttu-id="d1b71-137">Falso</span><span class="sxs-lookup"><span data-stu-id="d1b71-137">False</span></span>                               |
| <span data-ttu-id="d1b71-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d1b71-138">Is-Single-Valued</span></span>       | <span data-ttu-id="d1b71-139">Falso</span><span class="sxs-lookup"><span data-stu-id="d1b71-139">False</span></span>                               |
| <span data-ttu-id="d1b71-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="d1b71-140">Is Indexed</span></span>             | <span data-ttu-id="d1b71-141">Falso</span><span class="sxs-lookup"><span data-stu-id="d1b71-141">False</span></span>                               |
| <span data-ttu-id="d1b71-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d1b71-142">In Global Catalog</span></span>      | <span data-ttu-id="d1b71-143">Falso</span><span class="sxs-lookup"><span data-stu-id="d1b71-143">False</span></span>                               |
| <span data-ttu-id="d1b71-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d1b71-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1b71-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d1b71-145">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="d1b71-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1b71-146">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="d1b71-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1b71-147">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="d1b71-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1b71-148">Search-Flags</span></span>           | <span data-ttu-id="d1b71-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1b71-149">0x00000000</span></span>                          |
| <span data-ttu-id="d1b71-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1b71-150">System-Flags</span></span>           | <span data-ttu-id="d1b71-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1b71-151">0x00000010</span></span>                          |
| <span data-ttu-id="d1b71-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d1b71-152">Classes used in</span></span>        | [<span data-ttu-id="d1b71-153">**Group**</span><span class="sxs-lookup"><span data-stu-id="d1b71-153">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d1b71-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d1b71-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d1b71-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="d1b71-155">Entry</span></span> | <span data-ttu-id="d1b71-156">Valor</span><span class="sxs-lookup"><span data-stu-id="d1b71-156">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="d1b71-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="d1b71-157">Link-Id</span></span>                | <span data-ttu-id="d1b71-158">2014</span><span class="sxs-lookup"><span data-stu-id="d1b71-158">2014</span></span>                                |
| <span data-ttu-id="d1b71-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1b71-159">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="d1b71-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1b71-160">System-Only</span></span>            | <span data-ttu-id="d1b71-161">Falso</span><span class="sxs-lookup"><span data-stu-id="d1b71-161">False</span></span>                               |
| <span data-ttu-id="d1b71-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d1b71-162">Is-Single-Valued</span></span>       | <span data-ttu-id="d1b71-163">Falso</span><span class="sxs-lookup"><span data-stu-id="d1b71-163">False</span></span>                               |
| <span data-ttu-id="d1b71-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="d1b71-164">Is Indexed</span></span>             | <span data-ttu-id="d1b71-165">Falso</span><span class="sxs-lookup"><span data-stu-id="d1b71-165">False</span></span>                               |
| <span data-ttu-id="d1b71-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d1b71-166">In Global Catalog</span></span>      | <span data-ttu-id="d1b71-167">Falso</span><span class="sxs-lookup"><span data-stu-id="d1b71-167">False</span></span>                               |
| <span data-ttu-id="d1b71-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d1b71-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1b71-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d1b71-169">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="d1b71-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1b71-170">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="d1b71-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1b71-171">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="d1b71-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1b71-172">Search-Flags</span></span>           | <span data-ttu-id="d1b71-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1b71-173">0x00000000</span></span>                          |
| <span data-ttu-id="d1b71-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1b71-174">System-Flags</span></span>           | <span data-ttu-id="d1b71-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1b71-175">0x00000010</span></span>                          |
| <span data-ttu-id="d1b71-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d1b71-176">Classes used in</span></span>        | [<span data-ttu-id="d1b71-177">**Group**</span><span class="sxs-lookup"><span data-stu-id="d1b71-177">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d1b71-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1b71-178">Windows Server 2008</span></span>



| <span data-ttu-id="d1b71-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="d1b71-179">Entry</span></span> | <span data-ttu-id="d1b71-180">Valor</span><span class="sxs-lookup"><span data-stu-id="d1b71-180">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="d1b71-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="d1b71-181">Link-Id</span></span>                | <span data-ttu-id="d1b71-182">2014</span><span class="sxs-lookup"><span data-stu-id="d1b71-182">2014</span></span>                                |
| <span data-ttu-id="d1b71-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1b71-183">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="d1b71-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1b71-184">System-Only</span></span>            | <span data-ttu-id="d1b71-185">Falso</span><span class="sxs-lookup"><span data-stu-id="d1b71-185">False</span></span>                               |
| <span data-ttu-id="d1b71-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d1b71-186">Is-Single-Valued</span></span>       | <span data-ttu-id="d1b71-187">Falso</span><span class="sxs-lookup"><span data-stu-id="d1b71-187">False</span></span>                               |
| <span data-ttu-id="d1b71-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="d1b71-188">Is Indexed</span></span>             | <span data-ttu-id="d1b71-189">Falso</span><span class="sxs-lookup"><span data-stu-id="d1b71-189">False</span></span>                               |
| <span data-ttu-id="d1b71-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d1b71-190">In Global Catalog</span></span>      | <span data-ttu-id="d1b71-191">Falso</span><span class="sxs-lookup"><span data-stu-id="d1b71-191">False</span></span>                               |
| <span data-ttu-id="d1b71-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d1b71-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1b71-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d1b71-193">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="d1b71-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1b71-194">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="d1b71-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1b71-195">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="d1b71-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1b71-196">Search-Flags</span></span>           | <span data-ttu-id="d1b71-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1b71-197">0x00000000</span></span>                          |
| <span data-ttu-id="d1b71-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1b71-198">System-Flags</span></span>           | <span data-ttu-id="d1b71-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1b71-199">0x00000010</span></span>                          |
| <span data-ttu-id="d1b71-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d1b71-200">Classes used in</span></span>        | [<span data-ttu-id="d1b71-201">**Group**</span><span class="sxs-lookup"><span data-stu-id="d1b71-201">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d1b71-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d1b71-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d1b71-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="d1b71-203">Entry</span></span> | <span data-ttu-id="d1b71-204">Valor</span><span class="sxs-lookup"><span data-stu-id="d1b71-204">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="d1b71-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="d1b71-205">Link-Id</span></span>                | <span data-ttu-id="d1b71-206">2014</span><span class="sxs-lookup"><span data-stu-id="d1b71-206">2014</span></span>                                |
| <span data-ttu-id="d1b71-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1b71-207">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="d1b71-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1b71-208">System-Only</span></span>            | <span data-ttu-id="d1b71-209">Falso</span><span class="sxs-lookup"><span data-stu-id="d1b71-209">False</span></span>                               |
| <span data-ttu-id="d1b71-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d1b71-210">Is-Single-Valued</span></span>       | <span data-ttu-id="d1b71-211">Falso</span><span class="sxs-lookup"><span data-stu-id="d1b71-211">False</span></span>                               |
| <span data-ttu-id="d1b71-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="d1b71-212">Is Indexed</span></span>             | <span data-ttu-id="d1b71-213">Falso</span><span class="sxs-lookup"><span data-stu-id="d1b71-213">False</span></span>                               |
| <span data-ttu-id="d1b71-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d1b71-214">In Global Catalog</span></span>      | <span data-ttu-id="d1b71-215">Falso</span><span class="sxs-lookup"><span data-stu-id="d1b71-215">False</span></span>                               |
| <span data-ttu-id="d1b71-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d1b71-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1b71-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d1b71-217">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="d1b71-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1b71-218">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="d1b71-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1b71-219">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="d1b71-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1b71-220">Search-Flags</span></span>           | <span data-ttu-id="d1b71-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1b71-221">0x00000000</span></span>                          |
| <span data-ttu-id="d1b71-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1b71-222">System-Flags</span></span>           | <span data-ttu-id="d1b71-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1b71-223">0x00000010</span></span>                          |
| <span data-ttu-id="d1b71-224">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d1b71-224">Classes used in</span></span>        | [<span data-ttu-id="d1b71-225">**Group**</span><span class="sxs-lookup"><span data-stu-id="d1b71-225">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d1b71-226">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d1b71-226">Windows Server 2012</span></span>



| <span data-ttu-id="d1b71-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="d1b71-227">Entry</span></span> | <span data-ttu-id="d1b71-228">Valor</span><span class="sxs-lookup"><span data-stu-id="d1b71-228">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="d1b71-229">ID do link</span><span class="sxs-lookup"><span data-stu-id="d1b71-229">Link-Id</span></span>                | <span data-ttu-id="d1b71-230">2014</span><span class="sxs-lookup"><span data-stu-id="d1b71-230">2014</span></span>                                |
| <span data-ttu-id="d1b71-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d1b71-231">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="d1b71-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="d1b71-232">System-Only</span></span>            | <span data-ttu-id="d1b71-233">Falso</span><span class="sxs-lookup"><span data-stu-id="d1b71-233">False</span></span>                               |
| <span data-ttu-id="d1b71-234">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d1b71-234">Is-Single-Valued</span></span>       | <span data-ttu-id="d1b71-235">Falso</span><span class="sxs-lookup"><span data-stu-id="d1b71-235">False</span></span>                               |
| <span data-ttu-id="d1b71-236">É indexado</span><span class="sxs-lookup"><span data-stu-id="d1b71-236">Is Indexed</span></span>             | <span data-ttu-id="d1b71-237">Falso</span><span class="sxs-lookup"><span data-stu-id="d1b71-237">False</span></span>                               |
| <span data-ttu-id="d1b71-238">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d1b71-238">In Global Catalog</span></span>      | <span data-ttu-id="d1b71-239">Falso</span><span class="sxs-lookup"><span data-stu-id="d1b71-239">False</span></span>                               |
| <span data-ttu-id="d1b71-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d1b71-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="d1b71-241">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d1b71-241">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="d1b71-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d1b71-242">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="d1b71-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d1b71-243">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="d1b71-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d1b71-244">Search-Flags</span></span>           | <span data-ttu-id="d1b71-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1b71-245">0x00000000</span></span>                          |
| <span data-ttu-id="d1b71-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d1b71-246">System-Flags</span></span>           | <span data-ttu-id="d1b71-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1b71-247">0x00000010</span></span>                          |
| <span data-ttu-id="d1b71-248">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d1b71-248">Classes used in</span></span>        | [<span data-ttu-id="d1b71-249">**Group**</span><span class="sxs-lookup"><span data-stu-id="d1b71-249">**Group**</span></span>](c-group.md)<br/> |



 

 





