---
title: MS-DS-Replicas-NC-atributo Reason
description: Atributo do objeto ntdsConnection que indica por que (ou se) o KCC mostra que a conexão é útil na topologia de replicação. Tem vários valores e tem uma sintaxe Distname + binária, em que a parte binária é um campo de bits de tamanho int.
ms.assetid: ba66e346-d288-4c0b-b41e-599c3f8e8405
ms.tgt_platform: multiple
keywords:
- MS-DS-Replicas-NC-atributo Reason esquema do AD
- Esquema de AD do atributo mS-DS-ReplicatesNCReason
topic_type:
- apiref
api_name:
- MS-DS-Replicates-NC-Reason
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a45c587ef82773b5e7fd310e8e8591f18ad27ab
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104369956"
---
# <a name="ms-ds-replicates-nc-reason-attribute"></a><span data-ttu-id="90028-106">MS-DS-Replicas-NC-atributo Reason</span><span class="sxs-lookup"><span data-stu-id="90028-106">MS-DS-Replicates-NC-Reason attribute</span></span>

<span data-ttu-id="90028-107">Atributo do objeto ntdsConnection que indica por que (ou se) o KCC mostra que a conexão é útil na topologia de replicação.</span><span class="sxs-lookup"><span data-stu-id="90028-107">Attribute of ntdsConnection object that indicates why (or whether) the KCC shows the connection is useful in the replication topology.</span></span> <span data-ttu-id="90028-108">Tem vários valores e tem uma sintaxe Distname + binária, em que a parte binária é um campo de bits de tamanho int.</span><span class="sxs-lookup"><span data-stu-id="90028-108">Is multiple-valued and has DistName+Binary syntax, where the binary part is an int-size bitfield.</span></span>



| <span data-ttu-id="90028-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="90028-109">Entry</span></span> | <span data-ttu-id="90028-110">Valor</span><span class="sxs-lookup"><span data-stu-id="90028-110">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90028-111">CN</span><span class="sxs-lookup"><span data-stu-id="90028-111">CN</span></span>                | <span data-ttu-id="90028-112">MS-DS-Replicas-NC-Reason</span><span class="sxs-lookup"><span data-stu-id="90028-112">MS-DS-Replicates-NC-Reason</span></span>                                                                                                                 |
| <span data-ttu-id="90028-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="90028-113">Ldap-Display-Name</span></span> | <span data-ttu-id="90028-114">mS-DS-ReplicatesNCReason</span><span class="sxs-lookup"><span data-stu-id="90028-114">mS-DS-ReplicatesNCReason</span></span>                                                                                                                   |
| <span data-ttu-id="90028-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="90028-115">Size</span></span>              | <span data-ttu-id="90028-116">Valor para a parte binária: 0 = não \_ motivo, 1 = \_ topologia de GC, 2 = \_ topologia de anel, 4 = minimizar a \_ \_ topologia de saltos, 8 = topologia de servidores obsoletos \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="90028-116">Value for binary portion: 0 = NO\_REASON,1 = GC\_TOPOLOGY, 2 = RING\_TOPOLOGY, 4 = MINIMIZE\_HOPS\_TOPOLOGY, 8 = STALE\_SERVERS\_TOPOLOGY.</span></span> |
| <span data-ttu-id="90028-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="90028-117">Update Privilege</span></span>  | <span data-ttu-id="90028-118">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="90028-118">This value is set by the system.</span></span>                                                                                                           |
| <span data-ttu-id="90028-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="90028-119">Update Frequency</span></span>  | <span data-ttu-id="90028-120">Pode mudar em resposta a alterações na topologia de rede.</span><span class="sxs-lookup"><span data-stu-id="90028-120">Can change in response to changes in the network topology.</span></span>                                                                                 |
| <span data-ttu-id="90028-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="90028-121">Attribute-Id</span></span>      | <span data-ttu-id="90028-122">1.2.840.113556.1.4.1408</span><span class="sxs-lookup"><span data-stu-id="90028-122">1.2.840.113556.1.4.1408</span></span>                                                                                                                    |
| <span data-ttu-id="90028-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="90028-123">System-Id-Guid</span></span>    | <span data-ttu-id="90028-124">0ea12b84-08b3-11d3-91bc-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="90028-124">0ea12b84-08b3-11d3-91bc-0000f87a57d4</span></span>                                                                                                       |
| <span data-ttu-id="90028-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="90028-125">Syntax</span></span>            | [<span data-ttu-id="90028-126">**Objeto (DN-binário)**</span><span class="sxs-lookup"><span data-stu-id="90028-126">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md)                                                                                            |



## <a name="implementations"></a><span data-ttu-id="90028-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="90028-127">Implementations</span></span>

-   [<span data-ttu-id="90028-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="90028-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="90028-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="90028-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="90028-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="90028-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="90028-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="90028-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="90028-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="90028-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="90028-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="90028-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="90028-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="90028-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="90028-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="90028-135">Windows 2000 Server</span></span>



| <span data-ttu-id="90028-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="90028-136">Entry</span></span> | <span data-ttu-id="90028-137">Valor</span><span class="sxs-lookup"><span data-stu-id="90028-137">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="90028-138">ID do link</span><span class="sxs-lookup"><span data-stu-id="90028-138">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="90028-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90028-139">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="90028-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="90028-140">System-Only</span></span>            | <span data-ttu-id="90028-141">Falso</span><span class="sxs-lookup"><span data-stu-id="90028-141">False</span></span>                                                  |
| <span data-ttu-id="90028-142">É de valor único</span><span class="sxs-lookup"><span data-stu-id="90028-142">Is-Single-Valued</span></span>       | <span data-ttu-id="90028-143">Falso</span><span class="sxs-lookup"><span data-stu-id="90028-143">False</span></span>                                                  |
| <span data-ttu-id="90028-144">É indexado</span><span class="sxs-lookup"><span data-stu-id="90028-144">Is Indexed</span></span>             | <span data-ttu-id="90028-145">Falso</span><span class="sxs-lookup"><span data-stu-id="90028-145">False</span></span>                                                  |
| <span data-ttu-id="90028-146">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="90028-146">In Global Catalog</span></span>      | <span data-ttu-id="90028-147">Falso</span><span class="sxs-lookup"><span data-stu-id="90028-147">False</span></span>                                                  |
| <span data-ttu-id="90028-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="90028-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="90028-149">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="90028-149">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="90028-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90028-150">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="90028-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90028-151">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="90028-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90028-152">Search-Flags</span></span>           | <span data-ttu-id="90028-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90028-153">0x00000000</span></span>                                             |
| <span data-ttu-id="90028-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90028-154">System-Flags</span></span>           | <span data-ttu-id="90028-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90028-155">0x00000010</span></span>                                             |
| <span data-ttu-id="90028-156">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="90028-156">Classes used in</span></span>        | [<span data-ttu-id="90028-157">**NTDS-conexão**</span><span class="sxs-lookup"><span data-stu-id="90028-157">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="90028-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="90028-158">Windows Server 2003</span></span>



| <span data-ttu-id="90028-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="90028-159">Entry</span></span> | <span data-ttu-id="90028-160">Valor</span><span class="sxs-lookup"><span data-stu-id="90028-160">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="90028-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="90028-161">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="90028-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90028-162">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="90028-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="90028-163">System-Only</span></span>            | <span data-ttu-id="90028-164">Falso</span><span class="sxs-lookup"><span data-stu-id="90028-164">False</span></span>                                                  |
| <span data-ttu-id="90028-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="90028-165">Is-Single-Valued</span></span>       | <span data-ttu-id="90028-166">Falso</span><span class="sxs-lookup"><span data-stu-id="90028-166">False</span></span>                                                  |
| <span data-ttu-id="90028-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="90028-167">Is Indexed</span></span>             | <span data-ttu-id="90028-168">Falso</span><span class="sxs-lookup"><span data-stu-id="90028-168">False</span></span>                                                  |
| <span data-ttu-id="90028-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="90028-169">In Global Catalog</span></span>      | <span data-ttu-id="90028-170">Falso</span><span class="sxs-lookup"><span data-stu-id="90028-170">False</span></span>                                                  |
| <span data-ttu-id="90028-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="90028-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="90028-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="90028-172">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="90028-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90028-173">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="90028-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90028-174">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="90028-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90028-175">Search-Flags</span></span>           | <span data-ttu-id="90028-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90028-176">0x00000000</span></span>                                             |
| <span data-ttu-id="90028-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90028-177">System-Flags</span></span>           | <span data-ttu-id="90028-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90028-178">0x00000010</span></span>                                             |
| <span data-ttu-id="90028-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="90028-179">Classes used in</span></span>        | [<span data-ttu-id="90028-180">**NTDS-conexão**</span><span class="sxs-lookup"><span data-stu-id="90028-180">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="adam"></a><span data-ttu-id="90028-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="90028-181">ADAM</span></span>



| <span data-ttu-id="90028-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="90028-182">Entry</span></span> | <span data-ttu-id="90028-183">Valor</span><span class="sxs-lookup"><span data-stu-id="90028-183">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="90028-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="90028-184">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="90028-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90028-185">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="90028-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="90028-186">System-Only</span></span>            | <span data-ttu-id="90028-187">Falso</span><span class="sxs-lookup"><span data-stu-id="90028-187">False</span></span>                                                  |
| <span data-ttu-id="90028-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="90028-188">Is-Single-Valued</span></span>       | <span data-ttu-id="90028-189">Falso</span><span class="sxs-lookup"><span data-stu-id="90028-189">False</span></span>                                                  |
| <span data-ttu-id="90028-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="90028-190">Is Indexed</span></span>             | <span data-ttu-id="90028-191">Falso</span><span class="sxs-lookup"><span data-stu-id="90028-191">False</span></span>                                                  |
| <span data-ttu-id="90028-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="90028-192">In Global Catalog</span></span>      | <span data-ttu-id="90028-193">Falso</span><span class="sxs-lookup"><span data-stu-id="90028-193">False</span></span>                                                  |
| <span data-ttu-id="90028-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="90028-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="90028-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="90028-195">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="90028-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90028-196">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="90028-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90028-197">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="90028-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90028-198">Search-Flags</span></span>           | <span data-ttu-id="90028-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90028-199">0x00000000</span></span>                                             |
| <span data-ttu-id="90028-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90028-200">System-Flags</span></span>           | <span data-ttu-id="90028-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90028-201">0x00000010</span></span>                                             |
| <span data-ttu-id="90028-202">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="90028-202">Classes used in</span></span>        | [<span data-ttu-id="90028-203">**NTDS-conexão**</span><span class="sxs-lookup"><span data-stu-id="90028-203">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="90028-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="90028-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="90028-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="90028-205">Entry</span></span> | <span data-ttu-id="90028-206">Valor</span><span class="sxs-lookup"><span data-stu-id="90028-206">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="90028-207">ID do link</span><span class="sxs-lookup"><span data-stu-id="90028-207">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="90028-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90028-208">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="90028-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="90028-209">System-Only</span></span>            | <span data-ttu-id="90028-210">Falso</span><span class="sxs-lookup"><span data-stu-id="90028-210">False</span></span>                                                  |
| <span data-ttu-id="90028-211">É de valor único</span><span class="sxs-lookup"><span data-stu-id="90028-211">Is-Single-Valued</span></span>       | <span data-ttu-id="90028-212">Falso</span><span class="sxs-lookup"><span data-stu-id="90028-212">False</span></span>                                                  |
| <span data-ttu-id="90028-213">É indexado</span><span class="sxs-lookup"><span data-stu-id="90028-213">Is Indexed</span></span>             | <span data-ttu-id="90028-214">Falso</span><span class="sxs-lookup"><span data-stu-id="90028-214">False</span></span>                                                  |
| <span data-ttu-id="90028-215">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="90028-215">In Global Catalog</span></span>      | <span data-ttu-id="90028-216">Falso</span><span class="sxs-lookup"><span data-stu-id="90028-216">False</span></span>                                                  |
| <span data-ttu-id="90028-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="90028-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="90028-218">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="90028-218">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="90028-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90028-219">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="90028-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90028-220">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="90028-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90028-221">Search-Flags</span></span>           | <span data-ttu-id="90028-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90028-222">0x00000000</span></span>                                             |
| <span data-ttu-id="90028-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90028-223">System-Flags</span></span>           | <span data-ttu-id="90028-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90028-224">0x00000010</span></span>                                             |
| <span data-ttu-id="90028-225">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="90028-225">Classes used in</span></span>        | [<span data-ttu-id="90028-226">**NTDS-conexão**</span><span class="sxs-lookup"><span data-stu-id="90028-226">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="90028-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="90028-227">Windows Server 2008</span></span>



| <span data-ttu-id="90028-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="90028-228">Entry</span></span> | <span data-ttu-id="90028-229">Valor</span><span class="sxs-lookup"><span data-stu-id="90028-229">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="90028-230">ID do link</span><span class="sxs-lookup"><span data-stu-id="90028-230">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="90028-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90028-231">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="90028-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="90028-232">System-Only</span></span>            | <span data-ttu-id="90028-233">Falso</span><span class="sxs-lookup"><span data-stu-id="90028-233">False</span></span>                                                  |
| <span data-ttu-id="90028-234">É de valor único</span><span class="sxs-lookup"><span data-stu-id="90028-234">Is-Single-Valued</span></span>       | <span data-ttu-id="90028-235">Falso</span><span class="sxs-lookup"><span data-stu-id="90028-235">False</span></span>                                                  |
| <span data-ttu-id="90028-236">É indexado</span><span class="sxs-lookup"><span data-stu-id="90028-236">Is Indexed</span></span>             | <span data-ttu-id="90028-237">Falso</span><span class="sxs-lookup"><span data-stu-id="90028-237">False</span></span>                                                  |
| <span data-ttu-id="90028-238">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="90028-238">In Global Catalog</span></span>      | <span data-ttu-id="90028-239">Falso</span><span class="sxs-lookup"><span data-stu-id="90028-239">False</span></span>                                                  |
| <span data-ttu-id="90028-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="90028-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="90028-241">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="90028-241">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="90028-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90028-242">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="90028-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90028-243">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="90028-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90028-244">Search-Flags</span></span>           | <span data-ttu-id="90028-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90028-245">0x00000000</span></span>                                             |
| <span data-ttu-id="90028-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90028-246">System-Flags</span></span>           | <span data-ttu-id="90028-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90028-247">0x00000010</span></span>                                             |
| <span data-ttu-id="90028-248">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="90028-248">Classes used in</span></span>        | [<span data-ttu-id="90028-249">**NTDS-conexão**</span><span class="sxs-lookup"><span data-stu-id="90028-249">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="90028-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="90028-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="90028-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="90028-251">Entry</span></span> | <span data-ttu-id="90028-252">Valor</span><span class="sxs-lookup"><span data-stu-id="90028-252">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="90028-253">ID do link</span><span class="sxs-lookup"><span data-stu-id="90028-253">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="90028-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90028-254">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="90028-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="90028-255">System-Only</span></span>            | <span data-ttu-id="90028-256">Falso</span><span class="sxs-lookup"><span data-stu-id="90028-256">False</span></span>                                                  |
| <span data-ttu-id="90028-257">É de valor único</span><span class="sxs-lookup"><span data-stu-id="90028-257">Is-Single-Valued</span></span>       | <span data-ttu-id="90028-258">Falso</span><span class="sxs-lookup"><span data-stu-id="90028-258">False</span></span>                                                  |
| <span data-ttu-id="90028-259">É indexado</span><span class="sxs-lookup"><span data-stu-id="90028-259">Is Indexed</span></span>             | <span data-ttu-id="90028-260">Falso</span><span class="sxs-lookup"><span data-stu-id="90028-260">False</span></span>                                                  |
| <span data-ttu-id="90028-261">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="90028-261">In Global Catalog</span></span>      | <span data-ttu-id="90028-262">Falso</span><span class="sxs-lookup"><span data-stu-id="90028-262">False</span></span>                                                  |
| <span data-ttu-id="90028-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="90028-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="90028-264">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="90028-264">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="90028-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90028-265">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="90028-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90028-266">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="90028-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90028-267">Search-Flags</span></span>           | <span data-ttu-id="90028-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90028-268">0x00000000</span></span>                                             |
| <span data-ttu-id="90028-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90028-269">System-Flags</span></span>           | <span data-ttu-id="90028-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90028-270">0x00000010</span></span>                                             |
| <span data-ttu-id="90028-271">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="90028-271">Classes used in</span></span>        | [<span data-ttu-id="90028-272">**NTDS-conexão**</span><span class="sxs-lookup"><span data-stu-id="90028-272">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="90028-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="90028-273">Windows Server 2012</span></span>



| <span data-ttu-id="90028-274">Entrada</span><span class="sxs-lookup"><span data-stu-id="90028-274">Entry</span></span> | <span data-ttu-id="90028-275">Valor</span><span class="sxs-lookup"><span data-stu-id="90028-275">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="90028-276">ID do link</span><span class="sxs-lookup"><span data-stu-id="90028-276">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="90028-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90028-277">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="90028-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="90028-278">System-Only</span></span>            | <span data-ttu-id="90028-279">Falso</span><span class="sxs-lookup"><span data-stu-id="90028-279">False</span></span>                                                  |
| <span data-ttu-id="90028-280">É de valor único</span><span class="sxs-lookup"><span data-stu-id="90028-280">Is-Single-Valued</span></span>       | <span data-ttu-id="90028-281">Falso</span><span class="sxs-lookup"><span data-stu-id="90028-281">False</span></span>                                                  |
| <span data-ttu-id="90028-282">É indexado</span><span class="sxs-lookup"><span data-stu-id="90028-282">Is Indexed</span></span>             | <span data-ttu-id="90028-283">Falso</span><span class="sxs-lookup"><span data-stu-id="90028-283">False</span></span>                                                  |
| <span data-ttu-id="90028-284">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="90028-284">In Global Catalog</span></span>      | <span data-ttu-id="90028-285">Falso</span><span class="sxs-lookup"><span data-stu-id="90028-285">False</span></span>                                                  |
| <span data-ttu-id="90028-286">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="90028-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="90028-287">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="90028-287">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="90028-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90028-288">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="90028-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90028-289">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="90028-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90028-290">Search-Flags</span></span>           | <span data-ttu-id="90028-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90028-291">0x00000000</span></span>                                             |
| <span data-ttu-id="90028-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90028-292">System-Flags</span></span>           | <span data-ttu-id="90028-293">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90028-293">0x00000010</span></span>                                             |
| <span data-ttu-id="90028-294">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="90028-294">Classes used in</span></span>        | [<span data-ttu-id="90028-295">**NTDS-conexão**</span><span class="sxs-lookup"><span data-stu-id="90028-295">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



 

 





