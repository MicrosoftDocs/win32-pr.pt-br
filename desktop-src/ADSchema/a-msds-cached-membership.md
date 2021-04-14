---
title: ms-DS-cache-atributo de associação
description: O atributo ms-DS-cache-Membership é usado pelo gerente de contas de segurança para a expansão de grupo durante a avaliação do token.
ms.assetid: e54c5d55-d292-4a6e-942a-3818f5d75301
ms.tgt_platform: multiple
keywords:
- ms-DS-cache-atributo de associação do esquema do AD
- msDS-armazenado em cache-esquema de atributo do AD
topic_type:
- apiref
api_name:
- ms-DS-Cached-Membership
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 936c5c21d33d19ee51dba7f1dec0b03299cee346
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104500080"
---
# <a name="ms-ds-cached-membership-attribute"></a><span data-ttu-id="e98e8-105">ms-DS-cache-atributo de associação</span><span class="sxs-lookup"><span data-stu-id="e98e8-105">ms-DS-Cached-Membership attribute</span></span>

<span data-ttu-id="e98e8-106">O atributo **MS-DS-cache-Membership** é usado pelo gerente de contas de segurança para a expansão de grupo durante a avaliação do token.</span><span class="sxs-lookup"><span data-stu-id="e98e8-106">The **ms-DS-Cached-Membership** attribute is used by the Security Accounts Manager for group expansion during token evaluation.</span></span>



| <span data-ttu-id="e98e8-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="e98e8-107">Entry</span></span> | <span data-ttu-id="e98e8-108">Valor</span><span class="sxs-lookup"><span data-stu-id="e98e8-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="e98e8-109">CN</span><span class="sxs-lookup"><span data-stu-id="e98e8-109">CN</span></span>                | <span data-ttu-id="e98e8-110">ms-DS-cache-Membership</span><span class="sxs-lookup"><span data-stu-id="e98e8-110">ms-DS-Cached-Membership</span></span>                               |
| <span data-ttu-id="e98e8-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e98e8-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e98e8-112">msDS-armazenado em cache-Associação</span><span class="sxs-lookup"><span data-stu-id="e98e8-112">msDS-Cached-Membership</span></span>                                |
| <span data-ttu-id="e98e8-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="e98e8-113">Size</span></span>              | <span data-ttu-id="e98e8-114">BLOB binário de até 3 quilobytes.</span><span class="sxs-lookup"><span data-stu-id="e98e8-114">Binary BLOB of up to 3 kilobytes.</span></span>                     |
| <span data-ttu-id="e98e8-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="e98e8-115">Update Privilege</span></span>  | <span data-ttu-id="e98e8-116">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="e98e8-116">This value is set by the system.</span></span>                      |
| <span data-ttu-id="e98e8-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="e98e8-117">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="e98e8-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e98e8-118">Attribute-Id</span></span>      | <span data-ttu-id="e98e8-119">1.2.840.113556.1.4.1441</span><span class="sxs-lookup"><span data-stu-id="e98e8-119">1.2.840.113556.1.4.1441</span></span>                               |
| <span data-ttu-id="e98e8-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e98e8-120">System-Id-Guid</span></span>    | <span data-ttu-id="e98e8-121">69cab008-cdd4-4bc9-bab8-0ff37efe1b20</span><span class="sxs-lookup"><span data-stu-id="e98e8-121">69cab008-cdd4-4bc9-bab8-0ff37efe1b20</span></span>                  |
| <span data-ttu-id="e98e8-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="e98e8-122">Syntax</span></span>            | [<span data-ttu-id="e98e8-123">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="e98e8-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="e98e8-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="e98e8-124">Implementations</span></span>

-   [<span data-ttu-id="e98e8-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e98e8-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e98e8-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e98e8-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e98e8-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e98e8-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e98e8-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e98e8-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e98e8-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e98e8-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="e98e8-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e98e8-130">Windows Server 2003</span></span>



| <span data-ttu-id="e98e8-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="e98e8-131">Entry</span></span> | <span data-ttu-id="e98e8-132">Valor</span><span class="sxs-lookup"><span data-stu-id="e98e8-132">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e98e8-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="e98e8-133">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e98e8-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e98e8-134">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e98e8-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="e98e8-135">System-Only</span></span>            | <span data-ttu-id="e98e8-136">Falso</span><span class="sxs-lookup"><span data-stu-id="e98e8-136">False</span></span>                             |
| <span data-ttu-id="e98e8-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e98e8-137">Is-Single-Valued</span></span>       | <span data-ttu-id="e98e8-138">True</span><span class="sxs-lookup"><span data-stu-id="e98e8-138">True</span></span>                              |
| <span data-ttu-id="e98e8-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="e98e8-139">Is Indexed</span></span>             | <span data-ttu-id="e98e8-140">Falso</span><span class="sxs-lookup"><span data-stu-id="e98e8-140">False</span></span>                             |
| <span data-ttu-id="e98e8-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e98e8-141">In Global Catalog</span></span>      | <span data-ttu-id="e98e8-142">Falso</span><span class="sxs-lookup"><span data-stu-id="e98e8-142">False</span></span>                             |
| <span data-ttu-id="e98e8-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e98e8-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="e98e8-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e98e8-144">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e98e8-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e98e8-145">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e98e8-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e98e8-146">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e98e8-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e98e8-147">Search-Flags</span></span>           | <span data-ttu-id="e98e8-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e98e8-148">0x00000000</span></span>                        |
| <span data-ttu-id="e98e8-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e98e8-149">System-Flags</span></span>           | <span data-ttu-id="e98e8-150">0x00000011</span><span class="sxs-lookup"><span data-stu-id="e98e8-150">0x00000011</span></span>                        |
| <span data-ttu-id="e98e8-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e98e8-151">Classes used in</span></span>        | [<span data-ttu-id="e98e8-152">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="e98e8-152">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e98e8-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e98e8-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e98e8-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="e98e8-154">Entry</span></span> | <span data-ttu-id="e98e8-155">Valor</span><span class="sxs-lookup"><span data-stu-id="e98e8-155">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e98e8-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="e98e8-156">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e98e8-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e98e8-157">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e98e8-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="e98e8-158">System-Only</span></span>            | <span data-ttu-id="e98e8-159">Falso</span><span class="sxs-lookup"><span data-stu-id="e98e8-159">False</span></span>                             |
| <span data-ttu-id="e98e8-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e98e8-160">Is-Single-Valued</span></span>       | <span data-ttu-id="e98e8-161">True</span><span class="sxs-lookup"><span data-stu-id="e98e8-161">True</span></span>                              |
| <span data-ttu-id="e98e8-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="e98e8-162">Is Indexed</span></span>             | <span data-ttu-id="e98e8-163">Falso</span><span class="sxs-lookup"><span data-stu-id="e98e8-163">False</span></span>                             |
| <span data-ttu-id="e98e8-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e98e8-164">In Global Catalog</span></span>      | <span data-ttu-id="e98e8-165">Falso</span><span class="sxs-lookup"><span data-stu-id="e98e8-165">False</span></span>                             |
| <span data-ttu-id="e98e8-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e98e8-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="e98e8-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e98e8-167">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e98e8-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e98e8-168">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e98e8-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e98e8-169">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e98e8-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e98e8-170">Search-Flags</span></span>           | <span data-ttu-id="e98e8-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e98e8-171">0x00000000</span></span>                        |
| <span data-ttu-id="e98e8-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e98e8-172">System-Flags</span></span>           | <span data-ttu-id="e98e8-173">0x00000011</span><span class="sxs-lookup"><span data-stu-id="e98e8-173">0x00000011</span></span>                        |
| <span data-ttu-id="e98e8-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e98e8-174">Classes used in</span></span>        | [<span data-ttu-id="e98e8-175">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="e98e8-175">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e98e8-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e98e8-176">Windows Server 2008</span></span>



| <span data-ttu-id="e98e8-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="e98e8-177">Entry</span></span> | <span data-ttu-id="e98e8-178">Valor</span><span class="sxs-lookup"><span data-stu-id="e98e8-178">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e98e8-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="e98e8-179">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e98e8-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e98e8-180">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e98e8-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="e98e8-181">System-Only</span></span>            | <span data-ttu-id="e98e8-182">Falso</span><span class="sxs-lookup"><span data-stu-id="e98e8-182">False</span></span>                             |
| <span data-ttu-id="e98e8-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e98e8-183">Is-Single-Valued</span></span>       | <span data-ttu-id="e98e8-184">True</span><span class="sxs-lookup"><span data-stu-id="e98e8-184">True</span></span>                              |
| <span data-ttu-id="e98e8-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="e98e8-185">Is Indexed</span></span>             | <span data-ttu-id="e98e8-186">Falso</span><span class="sxs-lookup"><span data-stu-id="e98e8-186">False</span></span>                             |
| <span data-ttu-id="e98e8-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e98e8-187">In Global Catalog</span></span>      | <span data-ttu-id="e98e8-188">Falso</span><span class="sxs-lookup"><span data-stu-id="e98e8-188">False</span></span>                             |
| <span data-ttu-id="e98e8-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e98e8-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="e98e8-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e98e8-190">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e98e8-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e98e8-191">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e98e8-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e98e8-192">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e98e8-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e98e8-193">Search-Flags</span></span>           | <span data-ttu-id="e98e8-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e98e8-194">0x00000000</span></span>                        |
| <span data-ttu-id="e98e8-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e98e8-195">System-Flags</span></span>           | <span data-ttu-id="e98e8-196">0x00000011</span><span class="sxs-lookup"><span data-stu-id="e98e8-196">0x00000011</span></span>                        |
| <span data-ttu-id="e98e8-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e98e8-197">Classes used in</span></span>        | [<span data-ttu-id="e98e8-198">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="e98e8-198">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e98e8-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e98e8-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e98e8-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="e98e8-200">Entry</span></span> | <span data-ttu-id="e98e8-201">Valor</span><span class="sxs-lookup"><span data-stu-id="e98e8-201">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e98e8-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="e98e8-202">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e98e8-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e98e8-203">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e98e8-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="e98e8-204">System-Only</span></span>            | <span data-ttu-id="e98e8-205">Falso</span><span class="sxs-lookup"><span data-stu-id="e98e8-205">False</span></span>                             |
| <span data-ttu-id="e98e8-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e98e8-206">Is-Single-Valued</span></span>       | <span data-ttu-id="e98e8-207">True</span><span class="sxs-lookup"><span data-stu-id="e98e8-207">True</span></span>                              |
| <span data-ttu-id="e98e8-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="e98e8-208">Is Indexed</span></span>             | <span data-ttu-id="e98e8-209">Falso</span><span class="sxs-lookup"><span data-stu-id="e98e8-209">False</span></span>                             |
| <span data-ttu-id="e98e8-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e98e8-210">In Global Catalog</span></span>      | <span data-ttu-id="e98e8-211">Falso</span><span class="sxs-lookup"><span data-stu-id="e98e8-211">False</span></span>                             |
| <span data-ttu-id="e98e8-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e98e8-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="e98e8-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e98e8-213">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e98e8-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e98e8-214">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e98e8-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e98e8-215">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e98e8-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e98e8-216">Search-Flags</span></span>           | <span data-ttu-id="e98e8-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e98e8-217">0x00000000</span></span>                        |
| <span data-ttu-id="e98e8-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e98e8-218">System-Flags</span></span>           | <span data-ttu-id="e98e8-219">0x00000011</span><span class="sxs-lookup"><span data-stu-id="e98e8-219">0x00000011</span></span>                        |
| <span data-ttu-id="e98e8-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e98e8-220">Classes used in</span></span>        | [<span data-ttu-id="e98e8-221">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="e98e8-221">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e98e8-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e98e8-222">Windows Server 2012</span></span>



| <span data-ttu-id="e98e8-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="e98e8-223">Entry</span></span> | <span data-ttu-id="e98e8-224">Valor</span><span class="sxs-lookup"><span data-stu-id="e98e8-224">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e98e8-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="e98e8-225">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e98e8-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e98e8-226">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e98e8-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="e98e8-227">System-Only</span></span>            | <span data-ttu-id="e98e8-228">Falso</span><span class="sxs-lookup"><span data-stu-id="e98e8-228">False</span></span>                             |
| <span data-ttu-id="e98e8-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e98e8-229">Is-Single-Valued</span></span>       | <span data-ttu-id="e98e8-230">True</span><span class="sxs-lookup"><span data-stu-id="e98e8-230">True</span></span>                              |
| <span data-ttu-id="e98e8-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="e98e8-231">Is Indexed</span></span>             | <span data-ttu-id="e98e8-232">Falso</span><span class="sxs-lookup"><span data-stu-id="e98e8-232">False</span></span>                             |
| <span data-ttu-id="e98e8-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e98e8-233">In Global Catalog</span></span>      | <span data-ttu-id="e98e8-234">Falso</span><span class="sxs-lookup"><span data-stu-id="e98e8-234">False</span></span>                             |
| <span data-ttu-id="e98e8-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e98e8-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="e98e8-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e98e8-236">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e98e8-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e98e8-237">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e98e8-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e98e8-238">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e98e8-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e98e8-239">Search-Flags</span></span>           | <span data-ttu-id="e98e8-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e98e8-240">0x00000000</span></span>                        |
| <span data-ttu-id="e98e8-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e98e8-241">System-Flags</span></span>           | <span data-ttu-id="e98e8-242">0x00000011</span><span class="sxs-lookup"><span data-stu-id="e98e8-242">0x00000011</span></span>                        |
| <span data-ttu-id="e98e8-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e98e8-243">Classes used in</span></span>        | [<span data-ttu-id="e98e8-244">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="e98e8-244">**User**</span></span>](c-user.md)<br/> |



 

 





