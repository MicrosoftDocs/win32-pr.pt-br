---
title: MS-FRS-Hub-atributo de membro
description: O atributo ms-FRS-Hub-member é usado para registrar as configurações de topologia de NTFRS preferenciais.
ms.assetid: df8623e0-745a-46f8-a696-8f6e7014fd2b
ms.tgt_platform: multiple
keywords:
- MS-FRS-Hub-member atributo AD Schema
- msFRS-Hub-membro atributo AD Schema
topic_type:
- apiref
api_name:
- ms-FRS-Hub-Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56a211c5951ac589d00c4b8c92c031c80b2d1415
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105750997"
---
# <a name="ms-frs-hub-member-attribute"></a><span data-ttu-id="9ab43-105">MS-FRS-Hub-atributo de membro</span><span class="sxs-lookup"><span data-stu-id="9ab43-105">ms-FRS-Hub-Member attribute</span></span>

<span data-ttu-id="9ab43-106">O atributo **MS-FRS-Hub-member** é usado para registrar as configurações de topologia de NTFRS preferenciais.</span><span class="sxs-lookup"><span data-stu-id="9ab43-106">The **ms-FRS-Hub-Member** attribute is used to record the preferred NTFRS topology settings.</span></span> <span data-ttu-id="9ab43-107">Quando um membro do FRS é adicionado ou excluído a um conjunto de réplicas, esses atributos são chamados e os ajustes apropriados são feitos nas conexões entre o restante dos membros do FRS no conjunto de réplicas.</span><span class="sxs-lookup"><span data-stu-id="9ab43-107">When an FRS member gets added or deleted to a replica set, these attributes are referred and appropriate adjustments are made to the connections between the rest of the FRS members in the replica set.</span></span>



| <span data-ttu-id="9ab43-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="9ab43-108">Entry</span></span> | <span data-ttu-id="9ab43-109">Valor</span><span class="sxs-lookup"><span data-stu-id="9ab43-109">Value</span></span> |
|-------------------|--------------------------------------------------------------------|
| <span data-ttu-id="9ab43-110">CN</span><span class="sxs-lookup"><span data-stu-id="9ab43-110">CN</span></span>                | <span data-ttu-id="9ab43-111">MS-FRS-Hub-member</span><span class="sxs-lookup"><span data-stu-id="9ab43-111">ms-FRS-Hub-Member</span></span>                                                  |
| <span data-ttu-id="9ab43-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="9ab43-112">Ldap-Display-Name</span></span> | <span data-ttu-id="9ab43-113">msFRS-Hub-membro</span><span class="sxs-lookup"><span data-stu-id="9ab43-113">msFRS-Hub-Member</span></span>                                                   |
| <span data-ttu-id="9ab43-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="9ab43-114">Size</span></span>              | \-                                                                 |
| <span data-ttu-id="9ab43-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="9ab43-115">Update Privilege</span></span>  | <span data-ttu-id="9ab43-116">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="9ab43-116">Domain administrator</span></span>                                               |
| <span data-ttu-id="9ab43-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="9ab43-117">Update Frequency</span></span>  | <span data-ttu-id="9ab43-118">Quando o conjunto de réplicas é criado ou a topologia preferida é alterada.</span><span class="sxs-lookup"><span data-stu-id="9ab43-118">When the replica set is created or the preferred topology changes.</span></span> |
| <span data-ttu-id="9ab43-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9ab43-119">Attribute-Id</span></span>      | <span data-ttu-id="9ab43-120">1.2.840.113556.1.4.1693</span><span class="sxs-lookup"><span data-stu-id="9ab43-120">1.2.840.113556.1.4.1693</span></span>                                            |
| <span data-ttu-id="9ab43-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="9ab43-121">System-Id-Guid</span></span>    | <span data-ttu-id="9ab43-122">5643ff81-35b6-4ca9-9512-baf0bd0a2772</span><span class="sxs-lookup"><span data-stu-id="9ab43-122">5643ff81-35b6-4ca9-9512-baf0bd0a2772</span></span>                               |
| <span data-ttu-id="9ab43-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ab43-123">Syntax</span></span>            | [<span data-ttu-id="9ab43-124">**Objeto (DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="9ab43-124">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)                            |



## <a name="implementations"></a><span data-ttu-id="9ab43-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="9ab43-125">Implementations</span></span>

-   [<span data-ttu-id="9ab43-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9ab43-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9ab43-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9ab43-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9ab43-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9ab43-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9ab43-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9ab43-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9ab43-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9ab43-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="9ab43-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9ab43-131">Windows Server 2003</span></span>



| <span data-ttu-id="9ab43-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="9ab43-132">Entry</span></span> | <span data-ttu-id="9ab43-133">Valor</span><span class="sxs-lookup"><span data-stu-id="9ab43-133">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="9ab43-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="9ab43-134">Link-Id</span></span>                | <span data-ttu-id="9ab43-135">1046</span><span class="sxs-lookup"><span data-stu-id="9ab43-135">1046</span></span>                                                      |
| <span data-ttu-id="9ab43-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ab43-136">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="9ab43-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ab43-137">System-Only</span></span>            | <span data-ttu-id="9ab43-138">Falso</span><span class="sxs-lookup"><span data-stu-id="9ab43-138">False</span></span>                                                     |
| <span data-ttu-id="9ab43-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9ab43-139">Is-Single-Valued</span></span>       | <span data-ttu-id="9ab43-140">True</span><span class="sxs-lookup"><span data-stu-id="9ab43-140">True</span></span>                                                      |
| <span data-ttu-id="9ab43-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="9ab43-141">Is Indexed</span></span>             | <span data-ttu-id="9ab43-142">Falso</span><span class="sxs-lookup"><span data-stu-id="9ab43-142">False</span></span>                                                     |
| <span data-ttu-id="9ab43-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9ab43-143">In Global Catalog</span></span>      | <span data-ttu-id="9ab43-144">Falso</span><span class="sxs-lookup"><span data-stu-id="9ab43-144">False</span></span>                                                     |
| <span data-ttu-id="9ab43-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9ab43-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ab43-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9ab43-146">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="9ab43-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ab43-147">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="9ab43-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ab43-148">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="9ab43-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ab43-149">Search-Flags</span></span>           | <span data-ttu-id="9ab43-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ab43-150">0x00000000</span></span>                                                |
| <span data-ttu-id="9ab43-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ab43-151">System-Flags</span></span>           | <span data-ttu-id="9ab43-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ab43-152">0x00000000</span></span>                                                |
| <span data-ttu-id="9ab43-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9ab43-153">Classes used in</span></span>        | [<span data-ttu-id="9ab43-154">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="9ab43-154">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9ab43-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9ab43-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9ab43-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="9ab43-156">Entry</span></span> | <span data-ttu-id="9ab43-157">Valor</span><span class="sxs-lookup"><span data-stu-id="9ab43-157">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="9ab43-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="9ab43-158">Link-Id</span></span>                | <span data-ttu-id="9ab43-159">1046</span><span class="sxs-lookup"><span data-stu-id="9ab43-159">1046</span></span>                                                      |
| <span data-ttu-id="9ab43-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ab43-160">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="9ab43-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ab43-161">System-Only</span></span>            | <span data-ttu-id="9ab43-162">Falso</span><span class="sxs-lookup"><span data-stu-id="9ab43-162">False</span></span>                                                     |
| <span data-ttu-id="9ab43-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9ab43-163">Is-Single-Valued</span></span>       | <span data-ttu-id="9ab43-164">True</span><span class="sxs-lookup"><span data-stu-id="9ab43-164">True</span></span>                                                      |
| <span data-ttu-id="9ab43-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="9ab43-165">Is Indexed</span></span>             | <span data-ttu-id="9ab43-166">Falso</span><span class="sxs-lookup"><span data-stu-id="9ab43-166">False</span></span>                                                     |
| <span data-ttu-id="9ab43-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9ab43-167">In Global Catalog</span></span>      | <span data-ttu-id="9ab43-168">Falso</span><span class="sxs-lookup"><span data-stu-id="9ab43-168">False</span></span>                                                     |
| <span data-ttu-id="9ab43-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9ab43-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ab43-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9ab43-170">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="9ab43-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ab43-171">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="9ab43-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ab43-172">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="9ab43-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ab43-173">Search-Flags</span></span>           | <span data-ttu-id="9ab43-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ab43-174">0x00000000</span></span>                                                |
| <span data-ttu-id="9ab43-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ab43-175">System-Flags</span></span>           | <span data-ttu-id="9ab43-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ab43-176">0x00000000</span></span>                                                |
| <span data-ttu-id="9ab43-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9ab43-177">Classes used in</span></span>        | [<span data-ttu-id="9ab43-178">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="9ab43-178">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9ab43-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9ab43-179">Windows Server 2008</span></span>



| <span data-ttu-id="9ab43-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="9ab43-180">Entry</span></span> | <span data-ttu-id="9ab43-181">Valor</span><span class="sxs-lookup"><span data-stu-id="9ab43-181">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="9ab43-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="9ab43-182">Link-Id</span></span>                | <span data-ttu-id="9ab43-183">1046</span><span class="sxs-lookup"><span data-stu-id="9ab43-183">1046</span></span>                                                      |
| <span data-ttu-id="9ab43-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ab43-184">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="9ab43-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ab43-185">System-Only</span></span>            | <span data-ttu-id="9ab43-186">Falso</span><span class="sxs-lookup"><span data-stu-id="9ab43-186">False</span></span>                                                     |
| <span data-ttu-id="9ab43-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9ab43-187">Is-Single-Valued</span></span>       | <span data-ttu-id="9ab43-188">True</span><span class="sxs-lookup"><span data-stu-id="9ab43-188">True</span></span>                                                      |
| <span data-ttu-id="9ab43-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="9ab43-189">Is Indexed</span></span>             | <span data-ttu-id="9ab43-190">Falso</span><span class="sxs-lookup"><span data-stu-id="9ab43-190">False</span></span>                                                     |
| <span data-ttu-id="9ab43-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9ab43-191">In Global Catalog</span></span>      | <span data-ttu-id="9ab43-192">Falso</span><span class="sxs-lookup"><span data-stu-id="9ab43-192">False</span></span>                                                     |
| <span data-ttu-id="9ab43-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9ab43-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ab43-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9ab43-194">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="9ab43-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ab43-195">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="9ab43-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ab43-196">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="9ab43-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ab43-197">Search-Flags</span></span>           | <span data-ttu-id="9ab43-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ab43-198">0x00000000</span></span>                                                |
| <span data-ttu-id="9ab43-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ab43-199">System-Flags</span></span>           | <span data-ttu-id="9ab43-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ab43-200">0x00000000</span></span>                                                |
| <span data-ttu-id="9ab43-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9ab43-201">Classes used in</span></span>        | [<span data-ttu-id="9ab43-202">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="9ab43-202">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9ab43-203">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9ab43-203">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9ab43-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="9ab43-204">Entry</span></span> | <span data-ttu-id="9ab43-205">Valor</span><span class="sxs-lookup"><span data-stu-id="9ab43-205">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="9ab43-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="9ab43-206">Link-Id</span></span>                | <span data-ttu-id="9ab43-207">1046</span><span class="sxs-lookup"><span data-stu-id="9ab43-207">1046</span></span>                                                      |
| <span data-ttu-id="9ab43-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ab43-208">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="9ab43-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ab43-209">System-Only</span></span>            | <span data-ttu-id="9ab43-210">Falso</span><span class="sxs-lookup"><span data-stu-id="9ab43-210">False</span></span>                                                     |
| <span data-ttu-id="9ab43-211">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9ab43-211">Is-Single-Valued</span></span>       | <span data-ttu-id="9ab43-212">True</span><span class="sxs-lookup"><span data-stu-id="9ab43-212">True</span></span>                                                      |
| <span data-ttu-id="9ab43-213">É indexado</span><span class="sxs-lookup"><span data-stu-id="9ab43-213">Is Indexed</span></span>             | <span data-ttu-id="9ab43-214">Falso</span><span class="sxs-lookup"><span data-stu-id="9ab43-214">False</span></span>                                                     |
| <span data-ttu-id="9ab43-215">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9ab43-215">In Global Catalog</span></span>      | <span data-ttu-id="9ab43-216">Falso</span><span class="sxs-lookup"><span data-stu-id="9ab43-216">False</span></span>                                                     |
| <span data-ttu-id="9ab43-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9ab43-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ab43-218">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9ab43-218">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="9ab43-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ab43-219">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="9ab43-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ab43-220">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="9ab43-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ab43-221">Search-Flags</span></span>           | <span data-ttu-id="9ab43-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ab43-222">0x00000000</span></span>                                                |
| <span data-ttu-id="9ab43-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ab43-223">System-Flags</span></span>           | <span data-ttu-id="9ab43-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ab43-224">0x00000000</span></span>                                                |
| <span data-ttu-id="9ab43-225">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9ab43-225">Classes used in</span></span>        | [<span data-ttu-id="9ab43-226">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="9ab43-226">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9ab43-227">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9ab43-227">Windows Server 2012</span></span>



| <span data-ttu-id="9ab43-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="9ab43-228">Entry</span></span> | <span data-ttu-id="9ab43-229">Valor</span><span class="sxs-lookup"><span data-stu-id="9ab43-229">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="9ab43-230">ID do link</span><span class="sxs-lookup"><span data-stu-id="9ab43-230">Link-Id</span></span>                | <span data-ttu-id="9ab43-231">1046</span><span class="sxs-lookup"><span data-stu-id="9ab43-231">1046</span></span>                                                      |
| <span data-ttu-id="9ab43-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ab43-232">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="9ab43-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ab43-233">System-Only</span></span>            | <span data-ttu-id="9ab43-234">Falso</span><span class="sxs-lookup"><span data-stu-id="9ab43-234">False</span></span>                                                     |
| <span data-ttu-id="9ab43-235">É de valor único</span><span class="sxs-lookup"><span data-stu-id="9ab43-235">Is-Single-Valued</span></span>       | <span data-ttu-id="9ab43-236">True</span><span class="sxs-lookup"><span data-stu-id="9ab43-236">True</span></span>                                                      |
| <span data-ttu-id="9ab43-237">É indexado</span><span class="sxs-lookup"><span data-stu-id="9ab43-237">Is Indexed</span></span>             | <span data-ttu-id="9ab43-238">Falso</span><span class="sxs-lookup"><span data-stu-id="9ab43-238">False</span></span>                                                     |
| <span data-ttu-id="9ab43-239">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="9ab43-239">In Global Catalog</span></span>      | <span data-ttu-id="9ab43-240">Falso</span><span class="sxs-lookup"><span data-stu-id="9ab43-240">False</span></span>                                                     |
| <span data-ttu-id="9ab43-241">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="9ab43-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ab43-242">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="9ab43-242">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="9ab43-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ab43-243">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="9ab43-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ab43-244">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="9ab43-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ab43-245">Search-Flags</span></span>           | <span data-ttu-id="9ab43-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ab43-246">0x00000000</span></span>                                                |
| <span data-ttu-id="9ab43-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ab43-247">System-Flags</span></span>           | <span data-ttu-id="9ab43-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ab43-248">0x00000000</span></span>                                                |
| <span data-ttu-id="9ab43-249">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="9ab43-249">Classes used in</span></span>        | [<span data-ttu-id="9ab43-250">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="9ab43-250">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="9ab43-251">Comentários</span><span class="sxs-lookup"><span data-stu-id="9ab43-251">Remarks</span></span>

<span data-ttu-id="9ab43-252">Este é o nome distinto totalmente qualificado de um objeto [**de membro NTFRS**](c-ntfrsmember.md) .</span><span class="sxs-lookup"><span data-stu-id="9ab43-252">This is the fully qualified distinguished name of an [**NTFRS-Member**](c-ntfrsmember.md) object.</span></span> <span data-ttu-id="9ab43-253">O nome distinto está no formato "CN = *<computerGuid>* , CN = *<Dfs Link Name>* , CN = *<Dfs Root name>* , CN = volumes DFS, CN = serviço de replicação de arquivo, CN = System, DC =..."</span><span class="sxs-lookup"><span data-stu-id="9ab43-253">The distinguished name is in the format of "CN=*<computerGuid>*, CN=*<Dfs Link Name>*, CN=*<Dfs Root name>*, CN=DFS Volumes, CN=File Replication Service,CN=System, DC=..."</span></span>

 

 





