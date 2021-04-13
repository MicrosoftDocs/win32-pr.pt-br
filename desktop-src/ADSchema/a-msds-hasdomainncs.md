---
title: atributo ms-DS-is-Domain-NCs
description: Informações de replicação do serviço de diretório que detalham os contextos de nomeação de domínio presentes em um servidor específico.
ms.assetid: e5a7c371-5a37-466e-b56f-ee261b48e3b2
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo ms-DS-is-Domain-NCs
- atributo msDS-HasDomainNCs do AD Schema
topic_type:
- apiref
api_name:
- ms-DS-Has-Domain-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83b946286974cc6ba4e6d30484e7768a1daeccb6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104456218"
---
# <a name="ms-ds-has-domain-ncs-attribute"></a><span data-ttu-id="338ae-105">atributo ms-DS-is-Domain-NCs</span><span class="sxs-lookup"><span data-stu-id="338ae-105">ms-DS-Has-Domain-NCs attribute</span></span>

<span data-ttu-id="338ae-106">Informações de replicação do serviço de diretório que detalham os contextos de nomeação de domínio presentes em um servidor específico.</span><span class="sxs-lookup"><span data-stu-id="338ae-106">Directory service replication information that details the domain naming contexts present on a particular server.</span></span>



| <span data-ttu-id="338ae-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="338ae-107">Entry</span></span> | <span data-ttu-id="338ae-108">Valor</span><span class="sxs-lookup"><span data-stu-id="338ae-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="338ae-109">CN</span><span class="sxs-lookup"><span data-stu-id="338ae-109">CN</span></span>                | <span data-ttu-id="338ae-110">ms-DS-is-Domain-NCs</span><span class="sxs-lookup"><span data-stu-id="338ae-110">ms-DS-Has-Domain-NCs</span></span>                                |
| <span data-ttu-id="338ae-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="338ae-111">Ldap-Display-Name</span></span> | <span data-ttu-id="338ae-112">msDS-HasDomainNCs</span><span class="sxs-lookup"><span data-stu-id="338ae-112">msDS-HasDomainNCs</span></span>                                   |
| <span data-ttu-id="338ae-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="338ae-113">Size</span></span>              | \-                                                  |
| <span data-ttu-id="338ae-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="338ae-114">Update Privilege</span></span>  | <span data-ttu-id="338ae-115">Esse valor é definido pelo sistema</span><span class="sxs-lookup"><span data-stu-id="338ae-115">This value is set by the system</span></span>                     |
| <span data-ttu-id="338ae-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="338ae-116">Update Frequency</span></span>  | <span data-ttu-id="338ae-117">Ele é definido pelo DCPromo e nunca é modificado depois.</span><span class="sxs-lookup"><span data-stu-id="338ae-117">It is set by DCPromo and never modified thereafter.</span></span> |
| <span data-ttu-id="338ae-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="338ae-118">Attribute-Id</span></span>      | <span data-ttu-id="338ae-119">1.2.840.113556.1.4.1820</span><span class="sxs-lookup"><span data-stu-id="338ae-119">1.2.840.113556.1.4.1820</span></span>                             |
| <span data-ttu-id="338ae-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="338ae-120">System-Id-Guid</span></span>    | <span data-ttu-id="338ae-121">6f17e347-a842-4498-b8b3-15e007da4fed</span><span class="sxs-lookup"><span data-stu-id="338ae-121">6f17e347-a842-4498-b8b3-15e007da4fed</span></span>                |
| <span data-ttu-id="338ae-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="338ae-122">Syntax</span></span>            | [<span data-ttu-id="338ae-123">**Objeto (DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="338ae-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)             |



## <a name="implementations"></a><span data-ttu-id="338ae-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="338ae-124">Implementations</span></span>

-   [<span data-ttu-id="338ae-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="338ae-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="338ae-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="338ae-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="338ae-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="338ae-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="338ae-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="338ae-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="338ae-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="338ae-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="338ae-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="338ae-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="338ae-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="338ae-131">Windows Server 2003</span></span>



| <span data-ttu-id="338ae-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="338ae-132">Entry</span></span> | <span data-ttu-id="338ae-133">Valor</span><span class="sxs-lookup"><span data-stu-id="338ae-133">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="338ae-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="338ae-134">Link-Id</span></span>                | <span data-ttu-id="338ae-135">2026</span><span class="sxs-lookup"><span data-stu-id="338ae-135">2026</span></span>                                     |
| <span data-ttu-id="338ae-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="338ae-136">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="338ae-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="338ae-137">System-Only</span></span>            | <span data-ttu-id="338ae-138">True</span><span class="sxs-lookup"><span data-stu-id="338ae-138">True</span></span>                                     |
| <span data-ttu-id="338ae-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="338ae-139">Is-Single-Valued</span></span>       | <span data-ttu-id="338ae-140">Falso</span><span class="sxs-lookup"><span data-stu-id="338ae-140">False</span></span>                                    |
| <span data-ttu-id="338ae-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="338ae-141">Is Indexed</span></span>             | <span data-ttu-id="338ae-142">Falso</span><span class="sxs-lookup"><span data-stu-id="338ae-142">False</span></span>                                    |
| <span data-ttu-id="338ae-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="338ae-143">In Global Catalog</span></span>      | <span data-ttu-id="338ae-144">Falso</span><span class="sxs-lookup"><span data-stu-id="338ae-144">False</span></span>                                    |
| <span data-ttu-id="338ae-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="338ae-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="338ae-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="338ae-146">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="338ae-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="338ae-147">Range-Lower</span></span>            | <span data-ttu-id="338ae-148">4</span><span class="sxs-lookup"><span data-stu-id="338ae-148">4</span></span>                                        |
| <span data-ttu-id="338ae-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="338ae-149">Range-Upper</span></span>            | <span data-ttu-id="338ae-150">4</span><span class="sxs-lookup"><span data-stu-id="338ae-150">4</span></span>                                        |
| <span data-ttu-id="338ae-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="338ae-151">Search-Flags</span></span>           | <span data-ttu-id="338ae-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="338ae-152">0x00000000</span></span>                               |
| <span data-ttu-id="338ae-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="338ae-153">System-Flags</span></span>           | <span data-ttu-id="338ae-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="338ae-154">0x00000010</span></span>                               |
| <span data-ttu-id="338ae-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="338ae-155">Classes used in</span></span>        | [<span data-ttu-id="338ae-156">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="338ae-156">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="338ae-157">ADAM</span><span class="sxs-lookup"><span data-stu-id="338ae-157">ADAM</span></span>



| <span data-ttu-id="338ae-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="338ae-158">Entry</span></span> | <span data-ttu-id="338ae-159">Valor</span><span class="sxs-lookup"><span data-stu-id="338ae-159">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="338ae-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="338ae-160">Link-Id</span></span>                | <span data-ttu-id="338ae-161">2026</span><span class="sxs-lookup"><span data-stu-id="338ae-161">2026</span></span>                                     |
| <span data-ttu-id="338ae-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="338ae-162">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="338ae-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="338ae-163">System-Only</span></span>            | <span data-ttu-id="338ae-164">True</span><span class="sxs-lookup"><span data-stu-id="338ae-164">True</span></span>                                     |
| <span data-ttu-id="338ae-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="338ae-165">Is-Single-Valued</span></span>       | <span data-ttu-id="338ae-166">Falso</span><span class="sxs-lookup"><span data-stu-id="338ae-166">False</span></span>                                    |
| <span data-ttu-id="338ae-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="338ae-167">Is Indexed</span></span>             | <span data-ttu-id="338ae-168">Falso</span><span class="sxs-lookup"><span data-stu-id="338ae-168">False</span></span>                                    |
| <span data-ttu-id="338ae-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="338ae-169">In Global Catalog</span></span>      | <span data-ttu-id="338ae-170">Falso</span><span class="sxs-lookup"><span data-stu-id="338ae-170">False</span></span>                                    |
| <span data-ttu-id="338ae-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="338ae-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="338ae-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="338ae-172">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="338ae-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="338ae-173">Range-Lower</span></span>            | <span data-ttu-id="338ae-174">4</span><span class="sxs-lookup"><span data-stu-id="338ae-174">4</span></span>                                        |
| <span data-ttu-id="338ae-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="338ae-175">Range-Upper</span></span>            | <span data-ttu-id="338ae-176">4</span><span class="sxs-lookup"><span data-stu-id="338ae-176">4</span></span>                                        |
| <span data-ttu-id="338ae-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="338ae-177">Search-Flags</span></span>           | <span data-ttu-id="338ae-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="338ae-178">0x00000000</span></span>                               |
| <span data-ttu-id="338ae-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="338ae-179">System-Flags</span></span>           | <span data-ttu-id="338ae-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="338ae-180">0x00000010</span></span>                               |
| <span data-ttu-id="338ae-181">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="338ae-181">Classes used in</span></span>        | [<span data-ttu-id="338ae-182">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="338ae-182">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="338ae-183">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="338ae-183">Windows Server 2003 R2</span></span>



| <span data-ttu-id="338ae-184">Entrada</span><span class="sxs-lookup"><span data-stu-id="338ae-184">Entry</span></span> | <span data-ttu-id="338ae-185">Valor</span><span class="sxs-lookup"><span data-stu-id="338ae-185">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="338ae-186">ID do link</span><span class="sxs-lookup"><span data-stu-id="338ae-186">Link-Id</span></span>                | <span data-ttu-id="338ae-187">2026</span><span class="sxs-lookup"><span data-stu-id="338ae-187">2026</span></span>                                     |
| <span data-ttu-id="338ae-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="338ae-188">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="338ae-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="338ae-189">System-Only</span></span>            | <span data-ttu-id="338ae-190">True</span><span class="sxs-lookup"><span data-stu-id="338ae-190">True</span></span>                                     |
| <span data-ttu-id="338ae-191">É de valor único</span><span class="sxs-lookup"><span data-stu-id="338ae-191">Is-Single-Valued</span></span>       | <span data-ttu-id="338ae-192">Falso</span><span class="sxs-lookup"><span data-stu-id="338ae-192">False</span></span>                                    |
| <span data-ttu-id="338ae-193">É indexado</span><span class="sxs-lookup"><span data-stu-id="338ae-193">Is Indexed</span></span>             | <span data-ttu-id="338ae-194">Falso</span><span class="sxs-lookup"><span data-stu-id="338ae-194">False</span></span>                                    |
| <span data-ttu-id="338ae-195">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="338ae-195">In Global Catalog</span></span>      | <span data-ttu-id="338ae-196">Falso</span><span class="sxs-lookup"><span data-stu-id="338ae-196">False</span></span>                                    |
| <span data-ttu-id="338ae-197">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="338ae-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="338ae-198">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="338ae-198">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="338ae-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="338ae-199">Range-Lower</span></span>            | <span data-ttu-id="338ae-200">4</span><span class="sxs-lookup"><span data-stu-id="338ae-200">4</span></span>                                        |
| <span data-ttu-id="338ae-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="338ae-201">Range-Upper</span></span>            | <span data-ttu-id="338ae-202">4</span><span class="sxs-lookup"><span data-stu-id="338ae-202">4</span></span>                                        |
| <span data-ttu-id="338ae-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="338ae-203">Search-Flags</span></span>           | <span data-ttu-id="338ae-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="338ae-204">0x00000000</span></span>                               |
| <span data-ttu-id="338ae-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="338ae-205">System-Flags</span></span>           | <span data-ttu-id="338ae-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="338ae-206">0x00000010</span></span>                               |
| <span data-ttu-id="338ae-207">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="338ae-207">Classes used in</span></span>        | [<span data-ttu-id="338ae-208">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="338ae-208">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="338ae-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="338ae-209">Windows Server 2008</span></span>



| <span data-ttu-id="338ae-210">Entrada</span><span class="sxs-lookup"><span data-stu-id="338ae-210">Entry</span></span> | <span data-ttu-id="338ae-211">Valor</span><span class="sxs-lookup"><span data-stu-id="338ae-211">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="338ae-212">ID do link</span><span class="sxs-lookup"><span data-stu-id="338ae-212">Link-Id</span></span>                | <span data-ttu-id="338ae-213">2026</span><span class="sxs-lookup"><span data-stu-id="338ae-213">2026</span></span>                                     |
| <span data-ttu-id="338ae-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="338ae-214">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="338ae-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="338ae-215">System-Only</span></span>            | <span data-ttu-id="338ae-216">True</span><span class="sxs-lookup"><span data-stu-id="338ae-216">True</span></span>                                     |
| <span data-ttu-id="338ae-217">É de valor único</span><span class="sxs-lookup"><span data-stu-id="338ae-217">Is-Single-Valued</span></span>       | <span data-ttu-id="338ae-218">Falso</span><span class="sxs-lookup"><span data-stu-id="338ae-218">False</span></span>                                    |
| <span data-ttu-id="338ae-219">É indexado</span><span class="sxs-lookup"><span data-stu-id="338ae-219">Is Indexed</span></span>             | <span data-ttu-id="338ae-220">Falso</span><span class="sxs-lookup"><span data-stu-id="338ae-220">False</span></span>                                    |
| <span data-ttu-id="338ae-221">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="338ae-221">In Global Catalog</span></span>      | <span data-ttu-id="338ae-222">Falso</span><span class="sxs-lookup"><span data-stu-id="338ae-222">False</span></span>                                    |
| <span data-ttu-id="338ae-223">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="338ae-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="338ae-224">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="338ae-224">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="338ae-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="338ae-225">Range-Lower</span></span>            | <span data-ttu-id="338ae-226">4</span><span class="sxs-lookup"><span data-stu-id="338ae-226">4</span></span>                                        |
| <span data-ttu-id="338ae-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="338ae-227">Range-Upper</span></span>            | <span data-ttu-id="338ae-228">4</span><span class="sxs-lookup"><span data-stu-id="338ae-228">4</span></span>                                        |
| <span data-ttu-id="338ae-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="338ae-229">Search-Flags</span></span>           | <span data-ttu-id="338ae-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="338ae-230">0x00000000</span></span>                               |
| <span data-ttu-id="338ae-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="338ae-231">System-Flags</span></span>           | <span data-ttu-id="338ae-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="338ae-232">0x00000010</span></span>                               |
| <span data-ttu-id="338ae-233">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="338ae-233">Classes used in</span></span>        | [<span data-ttu-id="338ae-234">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="338ae-234">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="338ae-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="338ae-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="338ae-236">Entrada</span><span class="sxs-lookup"><span data-stu-id="338ae-236">Entry</span></span> | <span data-ttu-id="338ae-237">Valor</span><span class="sxs-lookup"><span data-stu-id="338ae-237">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="338ae-238">ID do link</span><span class="sxs-lookup"><span data-stu-id="338ae-238">Link-Id</span></span>                | <span data-ttu-id="338ae-239">2026</span><span class="sxs-lookup"><span data-stu-id="338ae-239">2026</span></span>                                     |
| <span data-ttu-id="338ae-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="338ae-240">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="338ae-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="338ae-241">System-Only</span></span>            | <span data-ttu-id="338ae-242">True</span><span class="sxs-lookup"><span data-stu-id="338ae-242">True</span></span>                                     |
| <span data-ttu-id="338ae-243">É de valor único</span><span class="sxs-lookup"><span data-stu-id="338ae-243">Is-Single-Valued</span></span>       | <span data-ttu-id="338ae-244">Falso</span><span class="sxs-lookup"><span data-stu-id="338ae-244">False</span></span>                                    |
| <span data-ttu-id="338ae-245">É indexado</span><span class="sxs-lookup"><span data-stu-id="338ae-245">Is Indexed</span></span>             | <span data-ttu-id="338ae-246">Falso</span><span class="sxs-lookup"><span data-stu-id="338ae-246">False</span></span>                                    |
| <span data-ttu-id="338ae-247">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="338ae-247">In Global Catalog</span></span>      | <span data-ttu-id="338ae-248">Falso</span><span class="sxs-lookup"><span data-stu-id="338ae-248">False</span></span>                                    |
| <span data-ttu-id="338ae-249">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="338ae-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="338ae-250">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="338ae-250">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="338ae-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="338ae-251">Range-Lower</span></span>            | <span data-ttu-id="338ae-252">4</span><span class="sxs-lookup"><span data-stu-id="338ae-252">4</span></span>                                        |
| <span data-ttu-id="338ae-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="338ae-253">Range-Upper</span></span>            | <span data-ttu-id="338ae-254">4</span><span class="sxs-lookup"><span data-stu-id="338ae-254">4</span></span>                                        |
| <span data-ttu-id="338ae-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="338ae-255">Search-Flags</span></span>           | <span data-ttu-id="338ae-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="338ae-256">0x00000000</span></span>                               |
| <span data-ttu-id="338ae-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="338ae-257">System-Flags</span></span>           | <span data-ttu-id="338ae-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="338ae-258">0x00000010</span></span>                               |
| <span data-ttu-id="338ae-259">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="338ae-259">Classes used in</span></span>        | [<span data-ttu-id="338ae-260">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="338ae-260">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="338ae-261">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="338ae-261">Windows Server 2012</span></span>



| <span data-ttu-id="338ae-262">Entrada</span><span class="sxs-lookup"><span data-stu-id="338ae-262">Entry</span></span> | <span data-ttu-id="338ae-263">Valor</span><span class="sxs-lookup"><span data-stu-id="338ae-263">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="338ae-264">ID do link</span><span class="sxs-lookup"><span data-stu-id="338ae-264">Link-Id</span></span>                | <span data-ttu-id="338ae-265">2026</span><span class="sxs-lookup"><span data-stu-id="338ae-265">2026</span></span>                                     |
| <span data-ttu-id="338ae-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="338ae-266">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="338ae-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="338ae-267">System-Only</span></span>            | <span data-ttu-id="338ae-268">True</span><span class="sxs-lookup"><span data-stu-id="338ae-268">True</span></span>                                     |
| <span data-ttu-id="338ae-269">É de valor único</span><span class="sxs-lookup"><span data-stu-id="338ae-269">Is-Single-Valued</span></span>       | <span data-ttu-id="338ae-270">Falso</span><span class="sxs-lookup"><span data-stu-id="338ae-270">False</span></span>                                    |
| <span data-ttu-id="338ae-271">É indexado</span><span class="sxs-lookup"><span data-stu-id="338ae-271">Is Indexed</span></span>             | <span data-ttu-id="338ae-272">Falso</span><span class="sxs-lookup"><span data-stu-id="338ae-272">False</span></span>                                    |
| <span data-ttu-id="338ae-273">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="338ae-273">In Global Catalog</span></span>      | <span data-ttu-id="338ae-274">Falso</span><span class="sxs-lookup"><span data-stu-id="338ae-274">False</span></span>                                    |
| <span data-ttu-id="338ae-275">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="338ae-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="338ae-276">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="338ae-276">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="338ae-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="338ae-277">Range-Lower</span></span>            | <span data-ttu-id="338ae-278">4</span><span class="sxs-lookup"><span data-stu-id="338ae-278">4</span></span>                                        |
| <span data-ttu-id="338ae-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="338ae-279">Range-Upper</span></span>            | <span data-ttu-id="338ae-280">4</span><span class="sxs-lookup"><span data-stu-id="338ae-280">4</span></span>                                        |
| <span data-ttu-id="338ae-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="338ae-281">Search-Flags</span></span>           | <span data-ttu-id="338ae-282">0x00000000</span><span class="sxs-lookup"><span data-stu-id="338ae-282">0x00000000</span></span>                               |
| <span data-ttu-id="338ae-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="338ae-283">System-Flags</span></span>           | <span data-ttu-id="338ae-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="338ae-284">0x00000010</span></span>                               |
| <span data-ttu-id="338ae-285">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="338ae-285">Classes used in</span></span>        | [<span data-ttu-id="338ae-286">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="338ae-286">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





