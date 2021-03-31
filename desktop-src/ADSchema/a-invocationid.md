---
title: Invocation-Id atributo
description: Usado para identificar exclusivamente cada diretório do Microsoft Exchange Server na organização.
ms.assetid: c069a57c-b9d0-49e9-8096-39b43f378573
ms.tgt_platform: multiple
keywords:
- Esquema de Invocation-Id do atributo AD
- atributo de AD de atributos de invocação
topic_type:
- apiref
api_name:
- Invocation-Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611589c466013ad46c0920a2da1e2250cf596214
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086672"
---
# <a name="invocation-id-attribute"></a><span data-ttu-id="2d77c-105">Invocation-Id atributo</span><span class="sxs-lookup"><span data-stu-id="2d77c-105">Invocation-Id attribute</span></span>

<span data-ttu-id="2d77c-106">Usado para identificar exclusivamente cada diretório do Microsoft Exchange Server na organização.</span><span class="sxs-lookup"><span data-stu-id="2d77c-106">Used to uniquely identify each Microsoft Exchange Server directory in the organization.</span></span>



| <span data-ttu-id="2d77c-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="2d77c-107">Entry</span></span> | <span data-ttu-id="2d77c-108">Valor</span><span class="sxs-lookup"><span data-stu-id="2d77c-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="2d77c-109">CN</span><span class="sxs-lookup"><span data-stu-id="2d77c-109">CN</span></span>                | <span data-ttu-id="2d77c-110">Invocation-Id</span><span class="sxs-lookup"><span data-stu-id="2d77c-110">Invocation-Id</span></span>                                         |
| <span data-ttu-id="2d77c-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2d77c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2d77c-112">invocationId</span><span class="sxs-lookup"><span data-stu-id="2d77c-112">invocationId</span></span>                                          |
| <span data-ttu-id="2d77c-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="2d77c-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="2d77c-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="2d77c-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="2d77c-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="2d77c-115">Update Frequency</span></span>  | <span data-ttu-id="2d77c-116">Quando o Exchange Server está instalado.</span><span class="sxs-lookup"><span data-stu-id="2d77c-116">When the Exchange Server is installed.</span></span>                |
| <span data-ttu-id="2d77c-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2d77c-117">Attribute-Id</span></span>      | <span data-ttu-id="2d77c-118">1.2.840.113556.1.2.115</span><span class="sxs-lookup"><span data-stu-id="2d77c-118">1.2.840.113556.1.2.115</span></span>                                |
| <span data-ttu-id="2d77c-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2d77c-119">System-Id-Guid</span></span>    | <span data-ttu-id="2d77c-120">bf96798e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="2d77c-120">bf96798e-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="2d77c-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d77c-121">Syntax</span></span>            | [<span data-ttu-id="2d77c-122">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="2d77c-122">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="2d77c-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="2d77c-123">Implementations</span></span>

-   [<span data-ttu-id="2d77c-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2d77c-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2d77c-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2d77c-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2d77c-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="2d77c-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="2d77c-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2d77c-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2d77c-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2d77c-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2d77c-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2d77c-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2d77c-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2d77c-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2d77c-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2d77c-131">Windows 2000 Server</span></span>



| <span data-ttu-id="2d77c-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="2d77c-132">Entry</span></span> | <span data-ttu-id="2d77c-133">Valor</span><span class="sxs-lookup"><span data-stu-id="2d77c-133">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="2d77c-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="2d77c-134">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="2d77c-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d77c-135">MAPI-Id</span></span>                | <span data-ttu-id="2d77c-136">0x80BF</span><span class="sxs-lookup"><span data-stu-id="2d77c-136">0x80BF</span></span>                                   |
| <span data-ttu-id="2d77c-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d77c-137">System-Only</span></span>            | <span data-ttu-id="2d77c-138">True</span><span class="sxs-lookup"><span data-stu-id="2d77c-138">True</span></span>                                     |
| <span data-ttu-id="2d77c-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2d77c-139">Is-Single-Valued</span></span>       | <span data-ttu-id="2d77c-140">True</span><span class="sxs-lookup"><span data-stu-id="2d77c-140">True</span></span>                                     |
| <span data-ttu-id="2d77c-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="2d77c-141">Is Indexed</span></span>             | <span data-ttu-id="2d77c-142">Falso</span><span class="sxs-lookup"><span data-stu-id="2d77c-142">False</span></span>                                    |
| <span data-ttu-id="2d77c-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2d77c-143">In Global Catalog</span></span>      | <span data-ttu-id="2d77c-144">Falso</span><span class="sxs-lookup"><span data-stu-id="2d77c-144">False</span></span>                                    |
| <span data-ttu-id="2d77c-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2d77c-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d77c-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2d77c-146">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="2d77c-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d77c-147">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="2d77c-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d77c-148">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="2d77c-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d77c-149">Search-Flags</span></span>           | <span data-ttu-id="2d77c-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2d77c-150">0x00000000</span></span>                               |
| <span data-ttu-id="2d77c-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d77c-151">System-Flags</span></span>           | <span data-ttu-id="2d77c-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2d77c-152">0x00000010</span></span>                               |
| <span data-ttu-id="2d77c-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2d77c-153">Classes used in</span></span>        | [<span data-ttu-id="2d77c-154">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="2d77c-154">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2d77c-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2d77c-155">Windows Server 2003</span></span>



| <span data-ttu-id="2d77c-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="2d77c-156">Entry</span></span> | <span data-ttu-id="2d77c-157">Valor</span><span class="sxs-lookup"><span data-stu-id="2d77c-157">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="2d77c-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="2d77c-158">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="2d77c-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d77c-159">MAPI-Id</span></span>                | <span data-ttu-id="2d77c-160">0x80BF</span><span class="sxs-lookup"><span data-stu-id="2d77c-160">0x80BF</span></span>                                   |
| <span data-ttu-id="2d77c-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d77c-161">System-Only</span></span>            | <span data-ttu-id="2d77c-162">True</span><span class="sxs-lookup"><span data-stu-id="2d77c-162">True</span></span>                                     |
| <span data-ttu-id="2d77c-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2d77c-163">Is-Single-Valued</span></span>       | <span data-ttu-id="2d77c-164">True</span><span class="sxs-lookup"><span data-stu-id="2d77c-164">True</span></span>                                     |
| <span data-ttu-id="2d77c-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="2d77c-165">Is Indexed</span></span>             | <span data-ttu-id="2d77c-166">True</span><span class="sxs-lookup"><span data-stu-id="2d77c-166">True</span></span>                                     |
| <span data-ttu-id="2d77c-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2d77c-167">In Global Catalog</span></span>      | <span data-ttu-id="2d77c-168">Falso</span><span class="sxs-lookup"><span data-stu-id="2d77c-168">False</span></span>                                    |
| <span data-ttu-id="2d77c-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2d77c-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d77c-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2d77c-170">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="2d77c-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d77c-171">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="2d77c-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d77c-172">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="2d77c-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d77c-173">Search-Flags</span></span>           | <span data-ttu-id="2d77c-174">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2d77c-174">0x00000001</span></span>                               |
| <span data-ttu-id="2d77c-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d77c-175">System-Flags</span></span>           | <span data-ttu-id="2d77c-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2d77c-176">0x00000010</span></span>                               |
| <span data-ttu-id="2d77c-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2d77c-177">Classes used in</span></span>        | [<span data-ttu-id="2d77c-178">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="2d77c-178">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="2d77c-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="2d77c-179">ADAM</span></span>



| <span data-ttu-id="2d77c-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="2d77c-180">Entry</span></span> | <span data-ttu-id="2d77c-181">Valor</span><span class="sxs-lookup"><span data-stu-id="2d77c-181">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="2d77c-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="2d77c-182">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="2d77c-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d77c-183">MAPI-Id</span></span>                | <span data-ttu-id="2d77c-184">0x80BF</span><span class="sxs-lookup"><span data-stu-id="2d77c-184">0x80BF</span></span>                                   |
| <span data-ttu-id="2d77c-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d77c-185">System-Only</span></span>            | <span data-ttu-id="2d77c-186">True</span><span class="sxs-lookup"><span data-stu-id="2d77c-186">True</span></span>                                     |
| <span data-ttu-id="2d77c-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2d77c-187">Is-Single-Valued</span></span>       | <span data-ttu-id="2d77c-188">True</span><span class="sxs-lookup"><span data-stu-id="2d77c-188">True</span></span>                                     |
| <span data-ttu-id="2d77c-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="2d77c-189">Is Indexed</span></span>             | <span data-ttu-id="2d77c-190">True</span><span class="sxs-lookup"><span data-stu-id="2d77c-190">True</span></span>                                     |
| <span data-ttu-id="2d77c-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2d77c-191">In Global Catalog</span></span>      | <span data-ttu-id="2d77c-192">Falso</span><span class="sxs-lookup"><span data-stu-id="2d77c-192">False</span></span>                                    |
| <span data-ttu-id="2d77c-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2d77c-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d77c-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2d77c-194">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="2d77c-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d77c-195">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="2d77c-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d77c-196">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="2d77c-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d77c-197">Search-Flags</span></span>           | <span data-ttu-id="2d77c-198">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2d77c-198">0x00000001</span></span>                               |
| <span data-ttu-id="2d77c-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d77c-199">System-Flags</span></span>           | <span data-ttu-id="2d77c-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2d77c-200">0x00000010</span></span>                               |
| <span data-ttu-id="2d77c-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2d77c-201">Classes used in</span></span>        | [<span data-ttu-id="2d77c-202">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="2d77c-202">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2d77c-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2d77c-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2d77c-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="2d77c-204">Entry</span></span> | <span data-ttu-id="2d77c-205">Valor</span><span class="sxs-lookup"><span data-stu-id="2d77c-205">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="2d77c-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="2d77c-206">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="2d77c-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d77c-207">MAPI-Id</span></span>                | <span data-ttu-id="2d77c-208">0x80BF</span><span class="sxs-lookup"><span data-stu-id="2d77c-208">0x80BF</span></span>                                   |
| <span data-ttu-id="2d77c-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d77c-209">System-Only</span></span>            | <span data-ttu-id="2d77c-210">True</span><span class="sxs-lookup"><span data-stu-id="2d77c-210">True</span></span>                                     |
| <span data-ttu-id="2d77c-211">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2d77c-211">Is-Single-Valued</span></span>       | <span data-ttu-id="2d77c-212">True</span><span class="sxs-lookup"><span data-stu-id="2d77c-212">True</span></span>                                     |
| <span data-ttu-id="2d77c-213">É indexado</span><span class="sxs-lookup"><span data-stu-id="2d77c-213">Is Indexed</span></span>             | <span data-ttu-id="2d77c-214">True</span><span class="sxs-lookup"><span data-stu-id="2d77c-214">True</span></span>                                     |
| <span data-ttu-id="2d77c-215">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2d77c-215">In Global Catalog</span></span>      | <span data-ttu-id="2d77c-216">Falso</span><span class="sxs-lookup"><span data-stu-id="2d77c-216">False</span></span>                                    |
| <span data-ttu-id="2d77c-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2d77c-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d77c-218">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2d77c-218">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="2d77c-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d77c-219">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="2d77c-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d77c-220">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="2d77c-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d77c-221">Search-Flags</span></span>           | <span data-ttu-id="2d77c-222">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2d77c-222">0x00000001</span></span>                               |
| <span data-ttu-id="2d77c-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d77c-223">System-Flags</span></span>           | <span data-ttu-id="2d77c-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2d77c-224">0x00000010</span></span>                               |
| <span data-ttu-id="2d77c-225">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2d77c-225">Classes used in</span></span>        | [<span data-ttu-id="2d77c-226">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="2d77c-226">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2d77c-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2d77c-227">Windows Server 2008</span></span>



| <span data-ttu-id="2d77c-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="2d77c-228">Entry</span></span> | <span data-ttu-id="2d77c-229">Valor</span><span class="sxs-lookup"><span data-stu-id="2d77c-229">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="2d77c-230">ID do link</span><span class="sxs-lookup"><span data-stu-id="2d77c-230">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="2d77c-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d77c-231">MAPI-Id</span></span>                | <span data-ttu-id="2d77c-232">0x80BF</span><span class="sxs-lookup"><span data-stu-id="2d77c-232">0x80BF</span></span>                                   |
| <span data-ttu-id="2d77c-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d77c-233">System-Only</span></span>            | <span data-ttu-id="2d77c-234">True</span><span class="sxs-lookup"><span data-stu-id="2d77c-234">True</span></span>                                     |
| <span data-ttu-id="2d77c-235">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2d77c-235">Is-Single-Valued</span></span>       | <span data-ttu-id="2d77c-236">True</span><span class="sxs-lookup"><span data-stu-id="2d77c-236">True</span></span>                                     |
| <span data-ttu-id="2d77c-237">É indexado</span><span class="sxs-lookup"><span data-stu-id="2d77c-237">Is Indexed</span></span>             | <span data-ttu-id="2d77c-238">True</span><span class="sxs-lookup"><span data-stu-id="2d77c-238">True</span></span>                                     |
| <span data-ttu-id="2d77c-239">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2d77c-239">In Global Catalog</span></span>      | <span data-ttu-id="2d77c-240">Falso</span><span class="sxs-lookup"><span data-stu-id="2d77c-240">False</span></span>                                    |
| <span data-ttu-id="2d77c-241">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2d77c-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d77c-242">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2d77c-242">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="2d77c-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d77c-243">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="2d77c-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d77c-244">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="2d77c-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d77c-245">Search-Flags</span></span>           | <span data-ttu-id="2d77c-246">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2d77c-246">0x00000001</span></span>                               |
| <span data-ttu-id="2d77c-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d77c-247">System-Flags</span></span>           | <span data-ttu-id="2d77c-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2d77c-248">0x00000010</span></span>                               |
| <span data-ttu-id="2d77c-249">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2d77c-249">Classes used in</span></span>        | [<span data-ttu-id="2d77c-250">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="2d77c-250">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2d77c-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2d77c-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2d77c-252">Entrada</span><span class="sxs-lookup"><span data-stu-id="2d77c-252">Entry</span></span> | <span data-ttu-id="2d77c-253">Valor</span><span class="sxs-lookup"><span data-stu-id="2d77c-253">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="2d77c-254">ID do link</span><span class="sxs-lookup"><span data-stu-id="2d77c-254">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="2d77c-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d77c-255">MAPI-Id</span></span>                | <span data-ttu-id="2d77c-256">0x80BF</span><span class="sxs-lookup"><span data-stu-id="2d77c-256">0x80BF</span></span>                                   |
| <span data-ttu-id="2d77c-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d77c-257">System-Only</span></span>            | <span data-ttu-id="2d77c-258">True</span><span class="sxs-lookup"><span data-stu-id="2d77c-258">True</span></span>                                     |
| <span data-ttu-id="2d77c-259">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2d77c-259">Is-Single-Valued</span></span>       | <span data-ttu-id="2d77c-260">True</span><span class="sxs-lookup"><span data-stu-id="2d77c-260">True</span></span>                                     |
| <span data-ttu-id="2d77c-261">É indexado</span><span class="sxs-lookup"><span data-stu-id="2d77c-261">Is Indexed</span></span>             | <span data-ttu-id="2d77c-262">True</span><span class="sxs-lookup"><span data-stu-id="2d77c-262">True</span></span>                                     |
| <span data-ttu-id="2d77c-263">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2d77c-263">In Global Catalog</span></span>      | <span data-ttu-id="2d77c-264">Falso</span><span class="sxs-lookup"><span data-stu-id="2d77c-264">False</span></span>                                    |
| <span data-ttu-id="2d77c-265">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2d77c-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d77c-266">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2d77c-266">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="2d77c-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d77c-267">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="2d77c-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d77c-268">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="2d77c-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d77c-269">Search-Flags</span></span>           | <span data-ttu-id="2d77c-270">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2d77c-270">0x00000001</span></span>                               |
| <span data-ttu-id="2d77c-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d77c-271">System-Flags</span></span>           | <span data-ttu-id="2d77c-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2d77c-272">0x00000010</span></span>                               |
| <span data-ttu-id="2d77c-273">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2d77c-273">Classes used in</span></span>        | [<span data-ttu-id="2d77c-274">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="2d77c-274">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2d77c-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2d77c-275">Windows Server 2012</span></span>



| <span data-ttu-id="2d77c-276">Entrada</span><span class="sxs-lookup"><span data-stu-id="2d77c-276">Entry</span></span> | <span data-ttu-id="2d77c-277">Valor</span><span class="sxs-lookup"><span data-stu-id="2d77c-277">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="2d77c-278">ID do link</span><span class="sxs-lookup"><span data-stu-id="2d77c-278">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="2d77c-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d77c-279">MAPI-Id</span></span>                | <span data-ttu-id="2d77c-280">0x80BF</span><span class="sxs-lookup"><span data-stu-id="2d77c-280">0x80BF</span></span>                                   |
| <span data-ttu-id="2d77c-281">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d77c-281">System-Only</span></span>            | <span data-ttu-id="2d77c-282">True</span><span class="sxs-lookup"><span data-stu-id="2d77c-282">True</span></span>                                     |
| <span data-ttu-id="2d77c-283">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2d77c-283">Is-Single-Valued</span></span>       | <span data-ttu-id="2d77c-284">True</span><span class="sxs-lookup"><span data-stu-id="2d77c-284">True</span></span>                                     |
| <span data-ttu-id="2d77c-285">É indexado</span><span class="sxs-lookup"><span data-stu-id="2d77c-285">Is Indexed</span></span>             | <span data-ttu-id="2d77c-286">True</span><span class="sxs-lookup"><span data-stu-id="2d77c-286">True</span></span>                                     |
| <span data-ttu-id="2d77c-287">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2d77c-287">In Global Catalog</span></span>      | <span data-ttu-id="2d77c-288">Falso</span><span class="sxs-lookup"><span data-stu-id="2d77c-288">False</span></span>                                    |
| <span data-ttu-id="2d77c-289">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2d77c-289">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d77c-290">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2d77c-290">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="2d77c-291">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d77c-291">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="2d77c-292">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d77c-292">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="2d77c-293">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d77c-293">Search-Flags</span></span>           | <span data-ttu-id="2d77c-294">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2d77c-294">0x00000001</span></span>                               |
| <span data-ttu-id="2d77c-295">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d77c-295">System-Flags</span></span>           | <span data-ttu-id="2d77c-296">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2d77c-296">0x00000010</span></span>                               |
| <span data-ttu-id="2d77c-297">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2d77c-297">Classes used in</span></span>        | [<span data-ttu-id="2d77c-298">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="2d77c-298">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





