---
title: Atributo removida-repl-DSA-Signatures
description: Controla as identidades de replicação DS anteriores de um determinado DC.
ms.assetid: 82e8b222-5635-41ad-b2ab-386c9e6aa280
ms.tgt_platform: multiple
keywords:
- Atributo AD removida-repl-DSA-Signatures
- Esquema de AD do atributo retiredReplDSASignatures
topic_type:
- apiref
api_name:
- Retired-Repl-DSA-Signatures
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a9a4cb4030a8d3aa24244bc2e7a2702e83686fc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104370002"
---
# <a name="retired-repl-dsa-signatures-attribute"></a><span data-ttu-id="8cc27-105">Atributo removida-repl-DSA-Signatures</span><span class="sxs-lookup"><span data-stu-id="8cc27-105">Retired-Repl-DSA-Signatures attribute</span></span>

<span data-ttu-id="8cc27-106">Controla as identidades de replicação DS anteriores de um determinado DC.</span><span class="sxs-lookup"><span data-stu-id="8cc27-106">Tracks the past DS replication identities of a given DC.</span></span>



| <span data-ttu-id="8cc27-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="8cc27-107">Entry</span></span> | <span data-ttu-id="8cc27-108">Valor</span><span class="sxs-lookup"><span data-stu-id="8cc27-108">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8cc27-109">CN</span><span class="sxs-lookup"><span data-stu-id="8cc27-109">CN</span></span>                | <span data-ttu-id="8cc27-110">Desativado-repl-DSA-Signatures</span><span class="sxs-lookup"><span data-stu-id="8cc27-110">Retired-Repl-DSA-Signatures</span></span>                                                         |
| <span data-ttu-id="8cc27-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8cc27-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8cc27-112">retiredReplDSASignatures</span><span class="sxs-lookup"><span data-stu-id="8cc27-112">retiredReplDSASignatures</span></span>                                                            |
| <span data-ttu-id="8cc27-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="8cc27-113">Size</span></span>              | <span data-ttu-id="8cc27-114">O comprimento é proporcional ao número de vezes que o DC foi restaurado do backup.</span><span class="sxs-lookup"><span data-stu-id="8cc27-114">Length is proportional to the number of times the DC has been restored from backup.</span></span> |
| <span data-ttu-id="8cc27-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="8cc27-115">Update Privilege</span></span>  | <span data-ttu-id="8cc27-116">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="8cc27-116">This value is set by the system.</span></span>                                                    |
| <span data-ttu-id="8cc27-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="8cc27-117">Update Frequency</span></span>  | \-                                                                                  |
| <span data-ttu-id="8cc27-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8cc27-118">Attribute-Id</span></span>      | <span data-ttu-id="8cc27-119">1.2.840.113556.1.4.673</span><span class="sxs-lookup"><span data-stu-id="8cc27-119">1.2.840.113556.1.4.673</span></span>                                                              |
| <span data-ttu-id="8cc27-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8cc27-120">System-Id-Guid</span></span>    | <span data-ttu-id="8cc27-121">7bfdcb7f-4807-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="8cc27-121">7bfdcb7f-4807-11d1-a9c3-0000f80367c1</span></span>                                                |
| <span data-ttu-id="8cc27-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="8cc27-122">Syntax</span></span>            | [<span data-ttu-id="8cc27-123">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="8cc27-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                               |



## <a name="implementations"></a><span data-ttu-id="8cc27-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="8cc27-124">Implementations</span></span>

-   [<span data-ttu-id="8cc27-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8cc27-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8cc27-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8cc27-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8cc27-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="8cc27-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="8cc27-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8cc27-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8cc27-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8cc27-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8cc27-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8cc27-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8cc27-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8cc27-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8cc27-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8cc27-132">Windows 2000 Server</span></span>



| <span data-ttu-id="8cc27-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="8cc27-133">Entry</span></span> | <span data-ttu-id="8cc27-134">Valor</span><span class="sxs-lookup"><span data-stu-id="8cc27-134">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="8cc27-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="8cc27-135">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="8cc27-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cc27-136">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="8cc27-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cc27-137">System-Only</span></span>            | <span data-ttu-id="8cc27-138">True</span><span class="sxs-lookup"><span data-stu-id="8cc27-138">True</span></span>                                     |
| <span data-ttu-id="8cc27-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8cc27-139">Is-Single-Valued</span></span>       | <span data-ttu-id="8cc27-140">True</span><span class="sxs-lookup"><span data-stu-id="8cc27-140">True</span></span>                                     |
| <span data-ttu-id="8cc27-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="8cc27-141">Is Indexed</span></span>             | <span data-ttu-id="8cc27-142">Falso</span><span class="sxs-lookup"><span data-stu-id="8cc27-142">False</span></span>                                    |
| <span data-ttu-id="8cc27-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8cc27-143">In Global Catalog</span></span>      | <span data-ttu-id="8cc27-144">Falso</span><span class="sxs-lookup"><span data-stu-id="8cc27-144">False</span></span>                                    |
| <span data-ttu-id="8cc27-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8cc27-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cc27-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8cc27-146">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="8cc27-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cc27-147">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="8cc27-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cc27-148">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="8cc27-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cc27-149">Search-Flags</span></span>           | <span data-ttu-id="8cc27-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cc27-150">0x00000000</span></span>                               |
| <span data-ttu-id="8cc27-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cc27-151">System-Flags</span></span>           | <span data-ttu-id="8cc27-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8cc27-152">0x00000010</span></span>                               |
| <span data-ttu-id="8cc27-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8cc27-153">Classes used in</span></span>        | [<span data-ttu-id="8cc27-154">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8cc27-154">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8cc27-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8cc27-155">Windows Server 2003</span></span>



| <span data-ttu-id="8cc27-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="8cc27-156">Entry</span></span> | <span data-ttu-id="8cc27-157">Valor</span><span class="sxs-lookup"><span data-stu-id="8cc27-157">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="8cc27-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="8cc27-158">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="8cc27-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cc27-159">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="8cc27-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cc27-160">System-Only</span></span>            | <span data-ttu-id="8cc27-161">True</span><span class="sxs-lookup"><span data-stu-id="8cc27-161">True</span></span>                                     |
| <span data-ttu-id="8cc27-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8cc27-162">Is-Single-Valued</span></span>       | <span data-ttu-id="8cc27-163">True</span><span class="sxs-lookup"><span data-stu-id="8cc27-163">True</span></span>                                     |
| <span data-ttu-id="8cc27-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="8cc27-164">Is Indexed</span></span>             | <span data-ttu-id="8cc27-165">Falso</span><span class="sxs-lookup"><span data-stu-id="8cc27-165">False</span></span>                                    |
| <span data-ttu-id="8cc27-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8cc27-166">In Global Catalog</span></span>      | <span data-ttu-id="8cc27-167">Falso</span><span class="sxs-lookup"><span data-stu-id="8cc27-167">False</span></span>                                    |
| <span data-ttu-id="8cc27-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8cc27-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cc27-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8cc27-169">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="8cc27-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cc27-170">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="8cc27-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cc27-171">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="8cc27-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cc27-172">Search-Flags</span></span>           | <span data-ttu-id="8cc27-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cc27-173">0x00000000</span></span>                               |
| <span data-ttu-id="8cc27-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cc27-174">System-Flags</span></span>           | <span data-ttu-id="8cc27-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8cc27-175">0x00000010</span></span>                               |
| <span data-ttu-id="8cc27-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8cc27-176">Classes used in</span></span>        | [<span data-ttu-id="8cc27-177">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8cc27-177">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="8cc27-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="8cc27-178">ADAM</span></span>



| <span data-ttu-id="8cc27-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="8cc27-179">Entry</span></span> | <span data-ttu-id="8cc27-180">Valor</span><span class="sxs-lookup"><span data-stu-id="8cc27-180">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="8cc27-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="8cc27-181">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="8cc27-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cc27-182">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="8cc27-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cc27-183">System-Only</span></span>            | <span data-ttu-id="8cc27-184">True</span><span class="sxs-lookup"><span data-stu-id="8cc27-184">True</span></span>                                     |
| <span data-ttu-id="8cc27-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8cc27-185">Is-Single-Valued</span></span>       | <span data-ttu-id="8cc27-186">True</span><span class="sxs-lookup"><span data-stu-id="8cc27-186">True</span></span>                                     |
| <span data-ttu-id="8cc27-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="8cc27-187">Is Indexed</span></span>             | <span data-ttu-id="8cc27-188">Falso</span><span class="sxs-lookup"><span data-stu-id="8cc27-188">False</span></span>                                    |
| <span data-ttu-id="8cc27-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8cc27-189">In Global Catalog</span></span>      | <span data-ttu-id="8cc27-190">Falso</span><span class="sxs-lookup"><span data-stu-id="8cc27-190">False</span></span>                                    |
| <span data-ttu-id="8cc27-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8cc27-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cc27-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8cc27-192">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="8cc27-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cc27-193">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="8cc27-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cc27-194">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="8cc27-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cc27-195">Search-Flags</span></span>           | <span data-ttu-id="8cc27-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cc27-196">0x00000000</span></span>                               |
| <span data-ttu-id="8cc27-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cc27-197">System-Flags</span></span>           | <span data-ttu-id="8cc27-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8cc27-198">0x00000010</span></span>                               |
| <span data-ttu-id="8cc27-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8cc27-199">Classes used in</span></span>        | [<span data-ttu-id="8cc27-200">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8cc27-200">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8cc27-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8cc27-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8cc27-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="8cc27-202">Entry</span></span> | <span data-ttu-id="8cc27-203">Valor</span><span class="sxs-lookup"><span data-stu-id="8cc27-203">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="8cc27-204">ID do link</span><span class="sxs-lookup"><span data-stu-id="8cc27-204">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="8cc27-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cc27-205">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="8cc27-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cc27-206">System-Only</span></span>            | <span data-ttu-id="8cc27-207">True</span><span class="sxs-lookup"><span data-stu-id="8cc27-207">True</span></span>                                     |
| <span data-ttu-id="8cc27-208">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8cc27-208">Is-Single-Valued</span></span>       | <span data-ttu-id="8cc27-209">True</span><span class="sxs-lookup"><span data-stu-id="8cc27-209">True</span></span>                                     |
| <span data-ttu-id="8cc27-210">É indexado</span><span class="sxs-lookup"><span data-stu-id="8cc27-210">Is Indexed</span></span>             | <span data-ttu-id="8cc27-211">Falso</span><span class="sxs-lookup"><span data-stu-id="8cc27-211">False</span></span>                                    |
| <span data-ttu-id="8cc27-212">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8cc27-212">In Global Catalog</span></span>      | <span data-ttu-id="8cc27-213">Falso</span><span class="sxs-lookup"><span data-stu-id="8cc27-213">False</span></span>                                    |
| <span data-ttu-id="8cc27-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8cc27-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cc27-215">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8cc27-215">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="8cc27-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cc27-216">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="8cc27-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cc27-217">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="8cc27-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cc27-218">Search-Flags</span></span>           | <span data-ttu-id="8cc27-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cc27-219">0x00000000</span></span>                               |
| <span data-ttu-id="8cc27-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cc27-220">System-Flags</span></span>           | <span data-ttu-id="8cc27-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8cc27-221">0x00000010</span></span>                               |
| <span data-ttu-id="8cc27-222">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8cc27-222">Classes used in</span></span>        | [<span data-ttu-id="8cc27-223">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8cc27-223">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8cc27-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8cc27-224">Windows Server 2008</span></span>



| <span data-ttu-id="8cc27-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="8cc27-225">Entry</span></span> | <span data-ttu-id="8cc27-226">Valor</span><span class="sxs-lookup"><span data-stu-id="8cc27-226">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="8cc27-227">ID do link</span><span class="sxs-lookup"><span data-stu-id="8cc27-227">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="8cc27-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cc27-228">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="8cc27-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cc27-229">System-Only</span></span>            | <span data-ttu-id="8cc27-230">True</span><span class="sxs-lookup"><span data-stu-id="8cc27-230">True</span></span>                                     |
| <span data-ttu-id="8cc27-231">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8cc27-231">Is-Single-Valued</span></span>       | <span data-ttu-id="8cc27-232">True</span><span class="sxs-lookup"><span data-stu-id="8cc27-232">True</span></span>                                     |
| <span data-ttu-id="8cc27-233">É indexado</span><span class="sxs-lookup"><span data-stu-id="8cc27-233">Is Indexed</span></span>             | <span data-ttu-id="8cc27-234">Falso</span><span class="sxs-lookup"><span data-stu-id="8cc27-234">False</span></span>                                    |
| <span data-ttu-id="8cc27-235">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8cc27-235">In Global Catalog</span></span>      | <span data-ttu-id="8cc27-236">Falso</span><span class="sxs-lookup"><span data-stu-id="8cc27-236">False</span></span>                                    |
| <span data-ttu-id="8cc27-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8cc27-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cc27-238">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8cc27-238">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="8cc27-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cc27-239">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="8cc27-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cc27-240">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="8cc27-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cc27-241">Search-Flags</span></span>           | <span data-ttu-id="8cc27-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cc27-242">0x00000000</span></span>                               |
| <span data-ttu-id="8cc27-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cc27-243">System-Flags</span></span>           | <span data-ttu-id="8cc27-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8cc27-244">0x00000010</span></span>                               |
| <span data-ttu-id="8cc27-245">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8cc27-245">Classes used in</span></span>        | [<span data-ttu-id="8cc27-246">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8cc27-246">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8cc27-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8cc27-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8cc27-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="8cc27-248">Entry</span></span> | <span data-ttu-id="8cc27-249">Valor</span><span class="sxs-lookup"><span data-stu-id="8cc27-249">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="8cc27-250">ID do link</span><span class="sxs-lookup"><span data-stu-id="8cc27-250">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="8cc27-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cc27-251">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="8cc27-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cc27-252">System-Only</span></span>            | <span data-ttu-id="8cc27-253">True</span><span class="sxs-lookup"><span data-stu-id="8cc27-253">True</span></span>                                     |
| <span data-ttu-id="8cc27-254">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8cc27-254">Is-Single-Valued</span></span>       | <span data-ttu-id="8cc27-255">True</span><span class="sxs-lookup"><span data-stu-id="8cc27-255">True</span></span>                                     |
| <span data-ttu-id="8cc27-256">É indexado</span><span class="sxs-lookup"><span data-stu-id="8cc27-256">Is Indexed</span></span>             | <span data-ttu-id="8cc27-257">Falso</span><span class="sxs-lookup"><span data-stu-id="8cc27-257">False</span></span>                                    |
| <span data-ttu-id="8cc27-258">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8cc27-258">In Global Catalog</span></span>      | <span data-ttu-id="8cc27-259">Falso</span><span class="sxs-lookup"><span data-stu-id="8cc27-259">False</span></span>                                    |
| <span data-ttu-id="8cc27-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8cc27-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cc27-261">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8cc27-261">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="8cc27-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cc27-262">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="8cc27-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cc27-263">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="8cc27-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cc27-264">Search-Flags</span></span>           | <span data-ttu-id="8cc27-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cc27-265">0x00000000</span></span>                               |
| <span data-ttu-id="8cc27-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cc27-266">System-Flags</span></span>           | <span data-ttu-id="8cc27-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8cc27-267">0x00000010</span></span>                               |
| <span data-ttu-id="8cc27-268">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8cc27-268">Classes used in</span></span>        | [<span data-ttu-id="8cc27-269">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8cc27-269">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8cc27-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8cc27-270">Windows Server 2012</span></span>



| <span data-ttu-id="8cc27-271">Entrada</span><span class="sxs-lookup"><span data-stu-id="8cc27-271">Entry</span></span> | <span data-ttu-id="8cc27-272">Valor</span><span class="sxs-lookup"><span data-stu-id="8cc27-272">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="8cc27-273">ID do link</span><span class="sxs-lookup"><span data-stu-id="8cc27-273">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="8cc27-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cc27-274">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="8cc27-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cc27-275">System-Only</span></span>            | <span data-ttu-id="8cc27-276">True</span><span class="sxs-lookup"><span data-stu-id="8cc27-276">True</span></span>                                     |
| <span data-ttu-id="8cc27-277">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8cc27-277">Is-Single-Valued</span></span>       | <span data-ttu-id="8cc27-278">True</span><span class="sxs-lookup"><span data-stu-id="8cc27-278">True</span></span>                                     |
| <span data-ttu-id="8cc27-279">É indexado</span><span class="sxs-lookup"><span data-stu-id="8cc27-279">Is Indexed</span></span>             | <span data-ttu-id="8cc27-280">Falso</span><span class="sxs-lookup"><span data-stu-id="8cc27-280">False</span></span>                                    |
| <span data-ttu-id="8cc27-281">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8cc27-281">In Global Catalog</span></span>      | <span data-ttu-id="8cc27-282">Falso</span><span class="sxs-lookup"><span data-stu-id="8cc27-282">False</span></span>                                    |
| <span data-ttu-id="8cc27-283">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8cc27-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cc27-284">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8cc27-284">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="8cc27-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cc27-285">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="8cc27-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cc27-286">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="8cc27-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cc27-287">Search-Flags</span></span>           | <span data-ttu-id="8cc27-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cc27-288">0x00000000</span></span>                               |
| <span data-ttu-id="8cc27-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cc27-289">System-Flags</span></span>           | <span data-ttu-id="8cc27-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8cc27-290">0x00000010</span></span>                               |
| <span data-ttu-id="8cc27-291">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8cc27-291">Classes used in</span></span>        | [<span data-ttu-id="8cc27-292">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8cc27-292">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





