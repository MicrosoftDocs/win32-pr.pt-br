---
title: ms-DS-tem-atributo-NCs-instanciado
description: Informações de estado de replicação DS, análogas a (e um superconjunto de) os atributos existentes hasMasterNCs e hasPartialReplicaNCs. A ser usado pelo KCC ao configurar parceiros de replicação.
ms.assetid: 00dda441-e382-4fb2-b735-ae547901c11f
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo ms-DS-tem-instancie-NCs
- atributo msDS-HasInstantiatedNCs do AD Schema
topic_type:
- apiref
api_name:
- ms-DS-Has-Instantiated-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2900d68f82e859bac7ce1dabbfea2d28fd8998b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104456217"
---
# <a name="ms-ds-has-instantiated-ncs-attribute"></a><span data-ttu-id="78e3c-106">ms-DS-tem-atributo-NCs-instanciado</span><span class="sxs-lookup"><span data-stu-id="78e3c-106">ms-DS-Has-Instantiated-NCs attribute</span></span>

<span data-ttu-id="78e3c-107">Informações de estado de replicação DS, análogas a (e um superconjunto de) os atributos existentes hasMasterNCs e hasPartialReplicaNCs.</span><span class="sxs-lookup"><span data-stu-id="78e3c-107">DS replication state information, analogous to (and a superset of) the existing attributes hasMasterNCs and hasPartialReplicaNCs.</span></span> <span data-ttu-id="78e3c-108">A ser usado pelo KCC ao configurar parceiros de replicação.</span><span class="sxs-lookup"><span data-stu-id="78e3c-108">To be used by the KCC when setting up replication partners.</span></span>



| <span data-ttu-id="78e3c-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="78e3c-109">Entry</span></span> | <span data-ttu-id="78e3c-110">Valor</span><span class="sxs-lookup"><span data-stu-id="78e3c-110">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78e3c-111">CN</span><span class="sxs-lookup"><span data-stu-id="78e3c-111">CN</span></span>                | <span data-ttu-id="78e3c-112">ms-DS-tem-NCs-instanciáveis</span><span class="sxs-lookup"><span data-stu-id="78e3c-112">ms-DS-Has-Instantiated-NCs</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="78e3c-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="78e3c-113">Ldap-Display-Name</span></span> | <span data-ttu-id="78e3c-114">msDS-HasInstantiatedNCs</span><span class="sxs-lookup"><span data-stu-id="78e3c-114">msDS-HasInstantiatedNCs</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="78e3c-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="78e3c-115">Size</span></span>              | <span data-ttu-id="78e3c-116">4 bytes</span><span class="sxs-lookup"><span data-stu-id="78e3c-116">4 bytes</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="78e3c-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="78e3c-117">Update Privilege</span></span>  | <span data-ttu-id="78e3c-118">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="78e3c-118">This value is set by the system.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="78e3c-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="78e3c-119">Update Frequency</span></span>  | <span data-ttu-id="78e3c-120">Aproximadamente duas vezes com a frequência de hasMasterNCs/hasPartialReplicaNCs.</span><span class="sxs-lookup"><span data-stu-id="78e3c-120">Roughly twice as often as hasMasterNCs / hasPartialReplicaNCs.</span></span> <span data-ttu-id="78e3c-121">Esses atributos existentes são atualizados somente quando o DC adiciona ou remove uma partição (por exemplo, ao mudar de DC para GC ou vice-versa).</span><span class="sxs-lookup"><span data-stu-id="78e3c-121">These existing attributes are updated only when the DC adds or removes a partition (For example, when changing from DC to GC or vice versa).</span></span> |
| <span data-ttu-id="78e3c-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="78e3c-122">Attribute-Id</span></span>      | <span data-ttu-id="78e3c-123">1.2.840.113556.1.4.1709</span><span class="sxs-lookup"><span data-stu-id="78e3c-123">1.2.840.113556.1.4.1709</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="78e3c-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="78e3c-124">System-Id-Guid</span></span>    | <span data-ttu-id="78e3c-125">11e9a5bc-4517-4049-af9c-51554fb0fc09</span><span class="sxs-lookup"><span data-stu-id="78e3c-125">11e9a5bc-4517-4049-af9c-51554fb0fc09</span></span>                                                                                                                                                                        |
| <span data-ttu-id="78e3c-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="78e3c-126">Syntax</span></span>            | [<span data-ttu-id="78e3c-127">**Objeto (DN-binário)**</span><span class="sxs-lookup"><span data-stu-id="78e3c-127">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md)                                                                                                                                                             |



## <a name="implementations"></a><span data-ttu-id="78e3c-128">Implementações</span><span class="sxs-lookup"><span data-stu-id="78e3c-128">Implementations</span></span>

-   [<span data-ttu-id="78e3c-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="78e3c-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="78e3c-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="78e3c-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="78e3c-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="78e3c-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="78e3c-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="78e3c-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="78e3c-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="78e3c-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="78e3c-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="78e3c-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="78e3c-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="78e3c-135">Windows Server 2003</span></span>



| <span data-ttu-id="78e3c-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="78e3c-136">Entry</span></span> | <span data-ttu-id="78e3c-137">Valor</span><span class="sxs-lookup"><span data-stu-id="78e3c-137">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="78e3c-138">ID do link</span><span class="sxs-lookup"><span data-stu-id="78e3c-138">Link-Id</span></span>                | <span data-ttu-id="78e3c-139">2002</span><span class="sxs-lookup"><span data-stu-id="78e3c-139">2002</span></span>                                     |
| <span data-ttu-id="78e3c-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78e3c-140">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="78e3c-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="78e3c-141">System-Only</span></span>            | <span data-ttu-id="78e3c-142">True</span><span class="sxs-lookup"><span data-stu-id="78e3c-142">True</span></span>                                     |
| <span data-ttu-id="78e3c-143">É de valor único</span><span class="sxs-lookup"><span data-stu-id="78e3c-143">Is-Single-Valued</span></span>       | <span data-ttu-id="78e3c-144">Falso</span><span class="sxs-lookup"><span data-stu-id="78e3c-144">False</span></span>                                    |
| <span data-ttu-id="78e3c-145">É indexado</span><span class="sxs-lookup"><span data-stu-id="78e3c-145">Is Indexed</span></span>             | <span data-ttu-id="78e3c-146">Falso</span><span class="sxs-lookup"><span data-stu-id="78e3c-146">False</span></span>                                    |
| <span data-ttu-id="78e3c-147">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="78e3c-147">In Global Catalog</span></span>      | <span data-ttu-id="78e3c-148">Falso</span><span class="sxs-lookup"><span data-stu-id="78e3c-148">False</span></span>                                    |
| <span data-ttu-id="78e3c-149">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="78e3c-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="78e3c-150">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="78e3c-150">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="78e3c-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78e3c-151">Range-Lower</span></span>            | <span data-ttu-id="78e3c-152">4</span><span class="sxs-lookup"><span data-stu-id="78e3c-152">4</span></span>                                        |
| <span data-ttu-id="78e3c-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78e3c-153">Range-Upper</span></span>            | <span data-ttu-id="78e3c-154">4</span><span class="sxs-lookup"><span data-stu-id="78e3c-154">4</span></span>                                        |
| <span data-ttu-id="78e3c-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78e3c-155">Search-Flags</span></span>           | <span data-ttu-id="78e3c-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78e3c-156">0x00000000</span></span>                               |
| <span data-ttu-id="78e3c-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78e3c-157">System-Flags</span></span>           | <span data-ttu-id="78e3c-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78e3c-158">0x00000010</span></span>                               |
| <span data-ttu-id="78e3c-159">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="78e3c-159">Classes used in</span></span>        | [<span data-ttu-id="78e3c-160">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="78e3c-160">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="78e3c-161">ADAM</span><span class="sxs-lookup"><span data-stu-id="78e3c-161">ADAM</span></span>



| <span data-ttu-id="78e3c-162">Entrada</span><span class="sxs-lookup"><span data-stu-id="78e3c-162">Entry</span></span> | <span data-ttu-id="78e3c-163">Valor</span><span class="sxs-lookup"><span data-stu-id="78e3c-163">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="78e3c-164">ID do link</span><span class="sxs-lookup"><span data-stu-id="78e3c-164">Link-Id</span></span>                | <span data-ttu-id="78e3c-165">2002</span><span class="sxs-lookup"><span data-stu-id="78e3c-165">2002</span></span>                                     |
| <span data-ttu-id="78e3c-166">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78e3c-166">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="78e3c-167">System-Only</span><span class="sxs-lookup"><span data-stu-id="78e3c-167">System-Only</span></span>            | <span data-ttu-id="78e3c-168">True</span><span class="sxs-lookup"><span data-stu-id="78e3c-168">True</span></span>                                     |
| <span data-ttu-id="78e3c-169">É de valor único</span><span class="sxs-lookup"><span data-stu-id="78e3c-169">Is-Single-Valued</span></span>       | <span data-ttu-id="78e3c-170">Falso</span><span class="sxs-lookup"><span data-stu-id="78e3c-170">False</span></span>                                    |
| <span data-ttu-id="78e3c-171">É indexado</span><span class="sxs-lookup"><span data-stu-id="78e3c-171">Is Indexed</span></span>             | <span data-ttu-id="78e3c-172">Falso</span><span class="sxs-lookup"><span data-stu-id="78e3c-172">False</span></span>                                    |
| <span data-ttu-id="78e3c-173">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="78e3c-173">In Global Catalog</span></span>      | <span data-ttu-id="78e3c-174">Falso</span><span class="sxs-lookup"><span data-stu-id="78e3c-174">False</span></span>                                    |
| <span data-ttu-id="78e3c-175">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="78e3c-175">NT-Security-Descriptor</span></span> | <span data-ttu-id="78e3c-176">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="78e3c-176">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="78e3c-177">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78e3c-177">Range-Lower</span></span>            | <span data-ttu-id="78e3c-178">4</span><span class="sxs-lookup"><span data-stu-id="78e3c-178">4</span></span>                                        |
| <span data-ttu-id="78e3c-179">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78e3c-179">Range-Upper</span></span>            | <span data-ttu-id="78e3c-180">4</span><span class="sxs-lookup"><span data-stu-id="78e3c-180">4</span></span>                                        |
| <span data-ttu-id="78e3c-181">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78e3c-181">Search-Flags</span></span>           | <span data-ttu-id="78e3c-182">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78e3c-182">0x00000000</span></span>                               |
| <span data-ttu-id="78e3c-183">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78e3c-183">System-Flags</span></span>           | <span data-ttu-id="78e3c-184">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78e3c-184">0x00000010</span></span>                               |
| <span data-ttu-id="78e3c-185">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="78e3c-185">Classes used in</span></span>        | [<span data-ttu-id="78e3c-186">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="78e3c-186">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="78e3c-187">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="78e3c-187">Windows Server 2003 R2</span></span>



| <span data-ttu-id="78e3c-188">Entrada</span><span class="sxs-lookup"><span data-stu-id="78e3c-188">Entry</span></span> | <span data-ttu-id="78e3c-189">Valor</span><span class="sxs-lookup"><span data-stu-id="78e3c-189">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="78e3c-190">ID do link</span><span class="sxs-lookup"><span data-stu-id="78e3c-190">Link-Id</span></span>                | <span data-ttu-id="78e3c-191">2002</span><span class="sxs-lookup"><span data-stu-id="78e3c-191">2002</span></span>                                     |
| <span data-ttu-id="78e3c-192">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78e3c-192">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="78e3c-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="78e3c-193">System-Only</span></span>            | <span data-ttu-id="78e3c-194">True</span><span class="sxs-lookup"><span data-stu-id="78e3c-194">True</span></span>                                     |
| <span data-ttu-id="78e3c-195">É de valor único</span><span class="sxs-lookup"><span data-stu-id="78e3c-195">Is-Single-Valued</span></span>       | <span data-ttu-id="78e3c-196">Falso</span><span class="sxs-lookup"><span data-stu-id="78e3c-196">False</span></span>                                    |
| <span data-ttu-id="78e3c-197">É indexado</span><span class="sxs-lookup"><span data-stu-id="78e3c-197">Is Indexed</span></span>             | <span data-ttu-id="78e3c-198">Falso</span><span class="sxs-lookup"><span data-stu-id="78e3c-198">False</span></span>                                    |
| <span data-ttu-id="78e3c-199">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="78e3c-199">In Global Catalog</span></span>      | <span data-ttu-id="78e3c-200">Falso</span><span class="sxs-lookup"><span data-stu-id="78e3c-200">False</span></span>                                    |
| <span data-ttu-id="78e3c-201">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="78e3c-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="78e3c-202">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="78e3c-202">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="78e3c-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78e3c-203">Range-Lower</span></span>            | <span data-ttu-id="78e3c-204">4</span><span class="sxs-lookup"><span data-stu-id="78e3c-204">4</span></span>                                        |
| <span data-ttu-id="78e3c-205">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78e3c-205">Range-Upper</span></span>            | <span data-ttu-id="78e3c-206">4</span><span class="sxs-lookup"><span data-stu-id="78e3c-206">4</span></span>                                        |
| <span data-ttu-id="78e3c-207">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78e3c-207">Search-Flags</span></span>           | <span data-ttu-id="78e3c-208">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78e3c-208">0x00000000</span></span>                               |
| <span data-ttu-id="78e3c-209">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78e3c-209">System-Flags</span></span>           | <span data-ttu-id="78e3c-210">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78e3c-210">0x00000010</span></span>                               |
| <span data-ttu-id="78e3c-211">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="78e3c-211">Classes used in</span></span>        | [<span data-ttu-id="78e3c-212">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="78e3c-212">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="78e3c-213">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78e3c-213">Windows Server 2008</span></span>



| <span data-ttu-id="78e3c-214">Entrada</span><span class="sxs-lookup"><span data-stu-id="78e3c-214">Entry</span></span> | <span data-ttu-id="78e3c-215">Valor</span><span class="sxs-lookup"><span data-stu-id="78e3c-215">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="78e3c-216">ID do link</span><span class="sxs-lookup"><span data-stu-id="78e3c-216">Link-Id</span></span>                | <span data-ttu-id="78e3c-217">2002</span><span class="sxs-lookup"><span data-stu-id="78e3c-217">2002</span></span>                                     |
| <span data-ttu-id="78e3c-218">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78e3c-218">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="78e3c-219">System-Only</span><span class="sxs-lookup"><span data-stu-id="78e3c-219">System-Only</span></span>            | <span data-ttu-id="78e3c-220">True</span><span class="sxs-lookup"><span data-stu-id="78e3c-220">True</span></span>                                     |
| <span data-ttu-id="78e3c-221">É de valor único</span><span class="sxs-lookup"><span data-stu-id="78e3c-221">Is-Single-Valued</span></span>       | <span data-ttu-id="78e3c-222">Falso</span><span class="sxs-lookup"><span data-stu-id="78e3c-222">False</span></span>                                    |
| <span data-ttu-id="78e3c-223">É indexado</span><span class="sxs-lookup"><span data-stu-id="78e3c-223">Is Indexed</span></span>             | <span data-ttu-id="78e3c-224">Falso</span><span class="sxs-lookup"><span data-stu-id="78e3c-224">False</span></span>                                    |
| <span data-ttu-id="78e3c-225">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="78e3c-225">In Global Catalog</span></span>      | <span data-ttu-id="78e3c-226">Falso</span><span class="sxs-lookup"><span data-stu-id="78e3c-226">False</span></span>                                    |
| <span data-ttu-id="78e3c-227">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="78e3c-227">NT-Security-Descriptor</span></span> | <span data-ttu-id="78e3c-228">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="78e3c-228">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="78e3c-229">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78e3c-229">Range-Lower</span></span>            | <span data-ttu-id="78e3c-230">4</span><span class="sxs-lookup"><span data-stu-id="78e3c-230">4</span></span>                                        |
| <span data-ttu-id="78e3c-231">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78e3c-231">Range-Upper</span></span>            | <span data-ttu-id="78e3c-232">4</span><span class="sxs-lookup"><span data-stu-id="78e3c-232">4</span></span>                                        |
| <span data-ttu-id="78e3c-233">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78e3c-233">Search-Flags</span></span>           | <span data-ttu-id="78e3c-234">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78e3c-234">0x00000000</span></span>                               |
| <span data-ttu-id="78e3c-235">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78e3c-235">System-Flags</span></span>           | <span data-ttu-id="78e3c-236">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78e3c-236">0x00000010</span></span>                               |
| <span data-ttu-id="78e3c-237">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="78e3c-237">Classes used in</span></span>        | [<span data-ttu-id="78e3c-238">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="78e3c-238">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="78e3c-239">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="78e3c-239">Windows Server 2008 R2</span></span>



| <span data-ttu-id="78e3c-240">Entrada</span><span class="sxs-lookup"><span data-stu-id="78e3c-240">Entry</span></span> | <span data-ttu-id="78e3c-241">Valor</span><span class="sxs-lookup"><span data-stu-id="78e3c-241">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="78e3c-242">ID do link</span><span class="sxs-lookup"><span data-stu-id="78e3c-242">Link-Id</span></span>                | <span data-ttu-id="78e3c-243">2002</span><span class="sxs-lookup"><span data-stu-id="78e3c-243">2002</span></span>                                     |
| <span data-ttu-id="78e3c-244">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78e3c-244">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="78e3c-245">System-Only</span><span class="sxs-lookup"><span data-stu-id="78e3c-245">System-Only</span></span>            | <span data-ttu-id="78e3c-246">True</span><span class="sxs-lookup"><span data-stu-id="78e3c-246">True</span></span>                                     |
| <span data-ttu-id="78e3c-247">É de valor único</span><span class="sxs-lookup"><span data-stu-id="78e3c-247">Is-Single-Valued</span></span>       | <span data-ttu-id="78e3c-248">Falso</span><span class="sxs-lookup"><span data-stu-id="78e3c-248">False</span></span>                                    |
| <span data-ttu-id="78e3c-249">É indexado</span><span class="sxs-lookup"><span data-stu-id="78e3c-249">Is Indexed</span></span>             | <span data-ttu-id="78e3c-250">Falso</span><span class="sxs-lookup"><span data-stu-id="78e3c-250">False</span></span>                                    |
| <span data-ttu-id="78e3c-251">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="78e3c-251">In Global Catalog</span></span>      | <span data-ttu-id="78e3c-252">Falso</span><span class="sxs-lookup"><span data-stu-id="78e3c-252">False</span></span>                                    |
| <span data-ttu-id="78e3c-253">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="78e3c-253">NT-Security-Descriptor</span></span> | <span data-ttu-id="78e3c-254">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="78e3c-254">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="78e3c-255">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78e3c-255">Range-Lower</span></span>            | <span data-ttu-id="78e3c-256">4</span><span class="sxs-lookup"><span data-stu-id="78e3c-256">4</span></span>                                        |
| <span data-ttu-id="78e3c-257">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78e3c-257">Range-Upper</span></span>            | <span data-ttu-id="78e3c-258">4</span><span class="sxs-lookup"><span data-stu-id="78e3c-258">4</span></span>                                        |
| <span data-ttu-id="78e3c-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78e3c-259">Search-Flags</span></span>           | <span data-ttu-id="78e3c-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78e3c-260">0x00000000</span></span>                               |
| <span data-ttu-id="78e3c-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78e3c-261">System-Flags</span></span>           | <span data-ttu-id="78e3c-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78e3c-262">0x00000010</span></span>                               |
| <span data-ttu-id="78e3c-263">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="78e3c-263">Classes used in</span></span>        | [<span data-ttu-id="78e3c-264">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="78e3c-264">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="78e3c-265">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="78e3c-265">Windows Server 2012</span></span>



| <span data-ttu-id="78e3c-266">Entrada</span><span class="sxs-lookup"><span data-stu-id="78e3c-266">Entry</span></span> | <span data-ttu-id="78e3c-267">Valor</span><span class="sxs-lookup"><span data-stu-id="78e3c-267">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="78e3c-268">ID do link</span><span class="sxs-lookup"><span data-stu-id="78e3c-268">Link-Id</span></span>                | <span data-ttu-id="78e3c-269">2002</span><span class="sxs-lookup"><span data-stu-id="78e3c-269">2002</span></span>                                     |
| <span data-ttu-id="78e3c-270">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78e3c-270">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="78e3c-271">System-Only</span><span class="sxs-lookup"><span data-stu-id="78e3c-271">System-Only</span></span>            | <span data-ttu-id="78e3c-272">True</span><span class="sxs-lookup"><span data-stu-id="78e3c-272">True</span></span>                                     |
| <span data-ttu-id="78e3c-273">É de valor único</span><span class="sxs-lookup"><span data-stu-id="78e3c-273">Is-Single-Valued</span></span>       | <span data-ttu-id="78e3c-274">Falso</span><span class="sxs-lookup"><span data-stu-id="78e3c-274">False</span></span>                                    |
| <span data-ttu-id="78e3c-275">É indexado</span><span class="sxs-lookup"><span data-stu-id="78e3c-275">Is Indexed</span></span>             | <span data-ttu-id="78e3c-276">Falso</span><span class="sxs-lookup"><span data-stu-id="78e3c-276">False</span></span>                                    |
| <span data-ttu-id="78e3c-277">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="78e3c-277">In Global Catalog</span></span>      | <span data-ttu-id="78e3c-278">Falso</span><span class="sxs-lookup"><span data-stu-id="78e3c-278">False</span></span>                                    |
| <span data-ttu-id="78e3c-279">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="78e3c-279">NT-Security-Descriptor</span></span> | <span data-ttu-id="78e3c-280">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="78e3c-280">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="78e3c-281">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78e3c-281">Range-Lower</span></span>            | <span data-ttu-id="78e3c-282">4</span><span class="sxs-lookup"><span data-stu-id="78e3c-282">4</span></span>                                        |
| <span data-ttu-id="78e3c-283">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78e3c-283">Range-Upper</span></span>            | <span data-ttu-id="78e3c-284">4</span><span class="sxs-lookup"><span data-stu-id="78e3c-284">4</span></span>                                        |
| <span data-ttu-id="78e3c-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78e3c-285">Search-Flags</span></span>           | <span data-ttu-id="78e3c-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78e3c-286">0x00000000</span></span>                               |
| <span data-ttu-id="78e3c-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78e3c-287">System-Flags</span></span>           | <span data-ttu-id="78e3c-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78e3c-288">0x00000010</span></span>                               |
| <span data-ttu-id="78e3c-289">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="78e3c-289">Classes used in</span></span>        | [<span data-ttu-id="78e3c-290">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="78e3c-290">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





