---
title: ms-DS-cache-Membership-atributo de carimbo de data/hora
description: O atributo ms-DS-cache-Membership-time-Timestamp é usado pelo gerente de contas de segurança para a expansão de grupo durante a avaliação do token.
ms.assetid: cb096f79-a57b-4001-b197-e75522904734
ms.tgt_platform: multiple
keywords:
- ms-DS-cache-Membership-atributo de carimbo de data/hora-esquema do AD
- msDS-cache-Membership-atributo de carimbo de data/hora-esquema do AD
topic_type:
- apiref
api_name:
- ms-DS-Cached-Membership-Time-Stamp
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 403e87288d906587a11f2a140a9f447ce8236aca
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105756453"
---
# <a name="ms-ds-cached-membership-time-stamp-attribute"></a><span data-ttu-id="18cc2-105">ms-DS-cache-Membership-atributo de carimbo de data/hora</span><span class="sxs-lookup"><span data-stu-id="18cc2-105">ms-DS-Cached-Membership-Time-Stamp attribute</span></span>

<span data-ttu-id="18cc2-106">O atributo **MS-DS-cache-Membership-time-timestamp** é usado pelo gerente de contas de segurança para a expansão de grupo durante a avaliação do token.</span><span class="sxs-lookup"><span data-stu-id="18cc2-106">The **ms-DS-Cached-Membership-Time-Stamp** attribute is used by the Security Accounts Manager for group expansion during token evaluation.</span></span>



| <span data-ttu-id="18cc2-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="18cc2-107">Entry</span></span> | <span data-ttu-id="18cc2-108">Valor</span><span class="sxs-lookup"><span data-stu-id="18cc2-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="18cc2-109">CN</span><span class="sxs-lookup"><span data-stu-id="18cc2-109">CN</span></span>                | <span data-ttu-id="18cc2-110">ms-DS-cache-Associação-carimbo de data/hora</span><span class="sxs-lookup"><span data-stu-id="18cc2-110">ms-DS-Cached-Membership-Time-Stamp</span></span>   |
| <span data-ttu-id="18cc2-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="18cc2-111">Ldap-Display-Name</span></span> | <span data-ttu-id="18cc2-112">msDS-armazenado em cache-Associação-carimbo de data/hora</span><span class="sxs-lookup"><span data-stu-id="18cc2-112">msDS-Cached-Membership-Time-Stamp</span></span>    |
| <span data-ttu-id="18cc2-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="18cc2-113">Size</span></span>              | <span data-ttu-id="18cc2-114">8 bytes</span><span class="sxs-lookup"><span data-stu-id="18cc2-114">8 bytes</span></span>                              |
| <span data-ttu-id="18cc2-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="18cc2-115">Update Privilege</span></span>  | <span data-ttu-id="18cc2-116">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="18cc2-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="18cc2-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="18cc2-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="18cc2-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="18cc2-118">Attribute-Id</span></span>      | <span data-ttu-id="18cc2-119">1.2.840.113556.1.4.1442</span><span class="sxs-lookup"><span data-stu-id="18cc2-119">1.2.840.113556.1.4.1442</span></span>              |
| <span data-ttu-id="18cc2-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="18cc2-120">System-Id-Guid</span></span>    | <span data-ttu-id="18cc2-121">3566bf1f-beee-4dcb-8abe-ef89fcfec6c1</span><span class="sxs-lookup"><span data-stu-id="18cc2-121">3566bf1f-beee-4dcb-8abe-ef89fcfec6c1</span></span> |
| <span data-ttu-id="18cc2-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="18cc2-122">Syntax</span></span>            | [<span data-ttu-id="18cc2-123">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="18cc2-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="18cc2-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="18cc2-124">Implementations</span></span>

-   [<span data-ttu-id="18cc2-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="18cc2-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="18cc2-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="18cc2-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="18cc2-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="18cc2-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="18cc2-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="18cc2-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="18cc2-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="18cc2-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="18cc2-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="18cc2-130">Windows Server 2003</span></span>



| <span data-ttu-id="18cc2-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="18cc2-131">Entry</span></span> | <span data-ttu-id="18cc2-132">Valor</span><span class="sxs-lookup"><span data-stu-id="18cc2-132">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="18cc2-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="18cc2-133">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="18cc2-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18cc2-134">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="18cc2-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="18cc2-135">System-Only</span></span>            | <span data-ttu-id="18cc2-136">Falso</span><span class="sxs-lookup"><span data-stu-id="18cc2-136">False</span></span>                             |
| <span data-ttu-id="18cc2-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="18cc2-137">Is-Single-Valued</span></span>       | <span data-ttu-id="18cc2-138">True</span><span class="sxs-lookup"><span data-stu-id="18cc2-138">True</span></span>                              |
| <span data-ttu-id="18cc2-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="18cc2-139">Is Indexed</span></span>             | <span data-ttu-id="18cc2-140">True</span><span class="sxs-lookup"><span data-stu-id="18cc2-140">True</span></span>                              |
| <span data-ttu-id="18cc2-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="18cc2-141">In Global Catalog</span></span>      | <span data-ttu-id="18cc2-142">Falso</span><span class="sxs-lookup"><span data-stu-id="18cc2-142">False</span></span>                             |
| <span data-ttu-id="18cc2-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="18cc2-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="18cc2-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="18cc2-144">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="18cc2-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18cc2-145">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="18cc2-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18cc2-146">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="18cc2-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18cc2-147">Search-Flags</span></span>           | <span data-ttu-id="18cc2-148">0x00000001</span><span class="sxs-lookup"><span data-stu-id="18cc2-148">0x00000001</span></span>                        |
| <span data-ttu-id="18cc2-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18cc2-149">System-Flags</span></span>           | <span data-ttu-id="18cc2-150">0x00000011</span><span class="sxs-lookup"><span data-stu-id="18cc2-150">0x00000011</span></span>                        |
| <span data-ttu-id="18cc2-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="18cc2-151">Classes used in</span></span>        | [<span data-ttu-id="18cc2-152">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="18cc2-152">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="18cc2-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="18cc2-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="18cc2-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="18cc2-154">Entry</span></span> | <span data-ttu-id="18cc2-155">Valor</span><span class="sxs-lookup"><span data-stu-id="18cc2-155">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="18cc2-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="18cc2-156">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="18cc2-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18cc2-157">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="18cc2-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="18cc2-158">System-Only</span></span>            | <span data-ttu-id="18cc2-159">Falso</span><span class="sxs-lookup"><span data-stu-id="18cc2-159">False</span></span>                             |
| <span data-ttu-id="18cc2-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="18cc2-160">Is-Single-Valued</span></span>       | <span data-ttu-id="18cc2-161">True</span><span class="sxs-lookup"><span data-stu-id="18cc2-161">True</span></span>                              |
| <span data-ttu-id="18cc2-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="18cc2-162">Is Indexed</span></span>             | <span data-ttu-id="18cc2-163">True</span><span class="sxs-lookup"><span data-stu-id="18cc2-163">True</span></span>                              |
| <span data-ttu-id="18cc2-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="18cc2-164">In Global Catalog</span></span>      | <span data-ttu-id="18cc2-165">Falso</span><span class="sxs-lookup"><span data-stu-id="18cc2-165">False</span></span>                             |
| <span data-ttu-id="18cc2-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="18cc2-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="18cc2-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="18cc2-167">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="18cc2-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18cc2-168">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="18cc2-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18cc2-169">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="18cc2-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18cc2-170">Search-Flags</span></span>           | <span data-ttu-id="18cc2-171">0x00000001</span><span class="sxs-lookup"><span data-stu-id="18cc2-171">0x00000001</span></span>                        |
| <span data-ttu-id="18cc2-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18cc2-172">System-Flags</span></span>           | <span data-ttu-id="18cc2-173">0x00000011</span><span class="sxs-lookup"><span data-stu-id="18cc2-173">0x00000011</span></span>                        |
| <span data-ttu-id="18cc2-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="18cc2-174">Classes used in</span></span>        | [<span data-ttu-id="18cc2-175">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="18cc2-175">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="18cc2-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18cc2-176">Windows Server 2008</span></span>



| <span data-ttu-id="18cc2-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="18cc2-177">Entry</span></span> | <span data-ttu-id="18cc2-178">Valor</span><span class="sxs-lookup"><span data-stu-id="18cc2-178">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="18cc2-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="18cc2-179">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="18cc2-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18cc2-180">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="18cc2-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="18cc2-181">System-Only</span></span>            | <span data-ttu-id="18cc2-182">Falso</span><span class="sxs-lookup"><span data-stu-id="18cc2-182">False</span></span>                             |
| <span data-ttu-id="18cc2-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="18cc2-183">Is-Single-Valued</span></span>       | <span data-ttu-id="18cc2-184">True</span><span class="sxs-lookup"><span data-stu-id="18cc2-184">True</span></span>                              |
| <span data-ttu-id="18cc2-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="18cc2-185">Is Indexed</span></span>             | <span data-ttu-id="18cc2-186">True</span><span class="sxs-lookup"><span data-stu-id="18cc2-186">True</span></span>                              |
| <span data-ttu-id="18cc2-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="18cc2-187">In Global Catalog</span></span>      | <span data-ttu-id="18cc2-188">Falso</span><span class="sxs-lookup"><span data-stu-id="18cc2-188">False</span></span>                             |
| <span data-ttu-id="18cc2-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="18cc2-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="18cc2-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="18cc2-190">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="18cc2-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18cc2-191">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="18cc2-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18cc2-192">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="18cc2-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18cc2-193">Search-Flags</span></span>           | <span data-ttu-id="18cc2-194">0x00000001</span><span class="sxs-lookup"><span data-stu-id="18cc2-194">0x00000001</span></span>                        |
| <span data-ttu-id="18cc2-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18cc2-195">System-Flags</span></span>           | <span data-ttu-id="18cc2-196">0x00000011</span><span class="sxs-lookup"><span data-stu-id="18cc2-196">0x00000011</span></span>                        |
| <span data-ttu-id="18cc2-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="18cc2-197">Classes used in</span></span>        | [<span data-ttu-id="18cc2-198">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="18cc2-198">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="18cc2-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="18cc2-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="18cc2-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="18cc2-200">Entry</span></span> | <span data-ttu-id="18cc2-201">Valor</span><span class="sxs-lookup"><span data-stu-id="18cc2-201">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="18cc2-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="18cc2-202">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="18cc2-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18cc2-203">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="18cc2-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="18cc2-204">System-Only</span></span>            | <span data-ttu-id="18cc2-205">Falso</span><span class="sxs-lookup"><span data-stu-id="18cc2-205">False</span></span>                             |
| <span data-ttu-id="18cc2-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="18cc2-206">Is-Single-Valued</span></span>       | <span data-ttu-id="18cc2-207">True</span><span class="sxs-lookup"><span data-stu-id="18cc2-207">True</span></span>                              |
| <span data-ttu-id="18cc2-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="18cc2-208">Is Indexed</span></span>             | <span data-ttu-id="18cc2-209">True</span><span class="sxs-lookup"><span data-stu-id="18cc2-209">True</span></span>                              |
| <span data-ttu-id="18cc2-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="18cc2-210">In Global Catalog</span></span>      | <span data-ttu-id="18cc2-211">Falso</span><span class="sxs-lookup"><span data-stu-id="18cc2-211">False</span></span>                             |
| <span data-ttu-id="18cc2-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="18cc2-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="18cc2-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="18cc2-213">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="18cc2-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18cc2-214">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="18cc2-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18cc2-215">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="18cc2-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18cc2-216">Search-Flags</span></span>           | <span data-ttu-id="18cc2-217">0x00000001</span><span class="sxs-lookup"><span data-stu-id="18cc2-217">0x00000001</span></span>                        |
| <span data-ttu-id="18cc2-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18cc2-218">System-Flags</span></span>           | <span data-ttu-id="18cc2-219">0x00000011</span><span class="sxs-lookup"><span data-stu-id="18cc2-219">0x00000011</span></span>                        |
| <span data-ttu-id="18cc2-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="18cc2-220">Classes used in</span></span>        | [<span data-ttu-id="18cc2-221">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="18cc2-221">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="18cc2-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="18cc2-222">Windows Server 2012</span></span>



| <span data-ttu-id="18cc2-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="18cc2-223">Entry</span></span> | <span data-ttu-id="18cc2-224">Valor</span><span class="sxs-lookup"><span data-stu-id="18cc2-224">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="18cc2-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="18cc2-225">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="18cc2-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18cc2-226">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="18cc2-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="18cc2-227">System-Only</span></span>            | <span data-ttu-id="18cc2-228">Falso</span><span class="sxs-lookup"><span data-stu-id="18cc2-228">False</span></span>                             |
| <span data-ttu-id="18cc2-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="18cc2-229">Is-Single-Valued</span></span>       | <span data-ttu-id="18cc2-230">True</span><span class="sxs-lookup"><span data-stu-id="18cc2-230">True</span></span>                              |
| <span data-ttu-id="18cc2-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="18cc2-231">Is Indexed</span></span>             | <span data-ttu-id="18cc2-232">True</span><span class="sxs-lookup"><span data-stu-id="18cc2-232">True</span></span>                              |
| <span data-ttu-id="18cc2-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="18cc2-233">In Global Catalog</span></span>      | <span data-ttu-id="18cc2-234">Falso</span><span class="sxs-lookup"><span data-stu-id="18cc2-234">False</span></span>                             |
| <span data-ttu-id="18cc2-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="18cc2-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="18cc2-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="18cc2-236">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="18cc2-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18cc2-237">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="18cc2-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18cc2-238">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="18cc2-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18cc2-239">Search-Flags</span></span>           | <span data-ttu-id="18cc2-240">0x00000001</span><span class="sxs-lookup"><span data-stu-id="18cc2-240">0x00000001</span></span>                        |
| <span data-ttu-id="18cc2-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18cc2-241">System-Flags</span></span>           | <span data-ttu-id="18cc2-242">0x00000011</span><span class="sxs-lookup"><span data-stu-id="18cc2-242">0x00000011</span></span>                        |
| <span data-ttu-id="18cc2-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="18cc2-243">Classes used in</span></span>        | [<span data-ttu-id="18cc2-244">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="18cc2-244">**User**</span></span>](c-user.md)<br/> |



 

 





