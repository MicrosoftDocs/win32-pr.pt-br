---
title: MS-DFSR-atributo Schedule
description: Contém o agendamento de replicação para o serviço de replicação do Sistema de Arquivos Distribuído (DFS).
ms.assetid: 6dfcce16-44a4-4f7a-93ba-0c0d50605682
ms.tgt_platform: multiple
keywords:
- MS-DFSR-agendar atributo AD Schema
- msDFSR-esquema de AD de atributos de agendamento
topic_type:
- apiref
api_name:
- ms-DFSR-Schedule
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 118ab92c656899d8275f0ff63ae43b412cf9742e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104456226"
---
# <a name="ms-dfsr-schedule-attribute"></a><span data-ttu-id="a6844-105">MS-DFSR-atributo Schedule</span><span class="sxs-lookup"><span data-stu-id="a6844-105">ms-DFSR-Schedule attribute</span></span>

<span data-ttu-id="a6844-106">Contém o agendamento de replicação para o serviço de replicação do Sistema de Arquivos Distribuído (DFS).</span><span class="sxs-lookup"><span data-stu-id="a6844-106">Contains the replication schedule for the Distributed File System (DFS) Replication service.</span></span>



| <span data-ttu-id="a6844-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="a6844-107">Entry</span></span> | <span data-ttu-id="a6844-108">Valor</span><span class="sxs-lookup"><span data-stu-id="a6844-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="a6844-109">CN</span><span class="sxs-lookup"><span data-stu-id="a6844-109">CN</span></span>                | <span data-ttu-id="a6844-110">MS-DFSR-Schedule</span><span class="sxs-lookup"><span data-stu-id="a6844-110">ms-DFSR-Schedule</span></span>                                      |
| <span data-ttu-id="a6844-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a6844-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a6844-112">msDFSR-agenda</span><span class="sxs-lookup"><span data-stu-id="a6844-112">msDFSR-Schedule</span></span>                                       |
| <span data-ttu-id="a6844-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="a6844-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="a6844-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="a6844-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="a6844-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="a6844-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="a6844-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a6844-116">Attribute-Id</span></span>      | <span data-ttu-id="a6844-117">1.2.840.113556.1.6.13.3.14</span><span class="sxs-lookup"><span data-stu-id="a6844-117">1.2.840.113556.1.6.13.3.14</span></span>                            |
| <span data-ttu-id="a6844-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a6844-118">System-Id-Guid</span></span>    | <span data-ttu-id="a6844-119">4699f15f-a71f-48e2-9ff5-5897c0759205</span><span class="sxs-lookup"><span data-stu-id="a6844-119">4699f15f-a71f-48e2-9ff5-5897c0759205</span></span>                  |
| <span data-ttu-id="a6844-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6844-120">Syntax</span></span>            | [<span data-ttu-id="a6844-121">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="a6844-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="a6844-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="a6844-122">Implementations</span></span>

-   [<span data-ttu-id="a6844-123">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a6844-123">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a6844-124">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a6844-124">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a6844-125">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a6844-125">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a6844-126">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a6844-126">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003-r2"></a><span data-ttu-id="a6844-127">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a6844-127">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a6844-128">Entrada</span><span class="sxs-lookup"><span data-stu-id="a6844-128">Entry</span></span> | <span data-ttu-id="a6844-129">Valor</span><span class="sxs-lookup"><span data-stu-id="a6844-129">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6844-130">ID do link</span><span class="sxs-lookup"><span data-stu-id="a6844-130">Link-Id</span></span>                | \-                                                                                                                                    |
| <span data-ttu-id="a6844-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a6844-131">MAPI-Id</span></span>                | \-                                                                                                                                    |
| <span data-ttu-id="a6844-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="a6844-132">System-Only</span></span>            | <span data-ttu-id="a6844-133">Falso</span><span class="sxs-lookup"><span data-stu-id="a6844-133">False</span></span>                                                                                                                                 |
| <span data-ttu-id="a6844-134">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a6844-134">Is-Single-Valued</span></span>       | <span data-ttu-id="a6844-135">True</span><span class="sxs-lookup"><span data-stu-id="a6844-135">True</span></span>                                                                                                                                  |
| <span data-ttu-id="a6844-136">É indexado</span><span class="sxs-lookup"><span data-stu-id="a6844-136">Is Indexed</span></span>             | <span data-ttu-id="a6844-137">Falso</span><span class="sxs-lookup"><span data-stu-id="a6844-137">False</span></span>                                                                                                                                 |
| <span data-ttu-id="a6844-138">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a6844-138">In Global Catalog</span></span>      | <span data-ttu-id="a6844-139">Falso</span><span class="sxs-lookup"><span data-stu-id="a6844-139">False</span></span>                                                                                                                                 |
| <span data-ttu-id="a6844-140">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a6844-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="a6844-141">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a6844-141">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="a6844-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a6844-142">Range-Lower</span></span>            | <span data-ttu-id="a6844-143">336</span><span class="sxs-lookup"><span data-stu-id="a6844-143">336</span></span>                                                                                                                                   |
| <span data-ttu-id="a6844-144">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a6844-144">Range-Upper</span></span>            | <span data-ttu-id="a6844-145">336</span><span class="sxs-lookup"><span data-stu-id="a6844-145">336</span></span>                                                                                                                                   |
| <span data-ttu-id="a6844-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a6844-146">Search-Flags</span></span>           | <span data-ttu-id="a6844-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a6844-147">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="a6844-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a6844-148">System-Flags</span></span>           | <span data-ttu-id="a6844-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a6844-149">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="a6844-150">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a6844-150">Classes used in</span></span>        | [<span data-ttu-id="a6844-151">**MS-DFSR-telereplication**</span><span class="sxs-lookup"><span data-stu-id="a6844-151">**ms-DFSR-ReplicationGroup**</span></span>](c-msdfsr-replicationgroup.md)<br/> [<span data-ttu-id="a6844-152">**MS-DFSR-Connection**</span><span class="sxs-lookup"><span data-stu-id="a6844-152">**ms-DFSR-Connection**</span></span>](c-msdfsr-connection.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a6844-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a6844-153">Windows Server 2008</span></span>



| <span data-ttu-id="a6844-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="a6844-154">Entry</span></span> | <span data-ttu-id="a6844-155">Valor</span><span class="sxs-lookup"><span data-stu-id="a6844-155">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6844-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="a6844-156">Link-Id</span></span>                | \-                                                                                                                                    |
| <span data-ttu-id="a6844-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a6844-157">MAPI-Id</span></span>                | \-                                                                                                                                    |
| <span data-ttu-id="a6844-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="a6844-158">System-Only</span></span>            | <span data-ttu-id="a6844-159">Falso</span><span class="sxs-lookup"><span data-stu-id="a6844-159">False</span></span>                                                                                                                                 |
| <span data-ttu-id="a6844-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a6844-160">Is-Single-Valued</span></span>       | <span data-ttu-id="a6844-161">True</span><span class="sxs-lookup"><span data-stu-id="a6844-161">True</span></span>                                                                                                                                  |
| <span data-ttu-id="a6844-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="a6844-162">Is Indexed</span></span>             | <span data-ttu-id="a6844-163">Falso</span><span class="sxs-lookup"><span data-stu-id="a6844-163">False</span></span>                                                                                                                                 |
| <span data-ttu-id="a6844-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a6844-164">In Global Catalog</span></span>      | <span data-ttu-id="a6844-165">Falso</span><span class="sxs-lookup"><span data-stu-id="a6844-165">False</span></span>                                                                                                                                 |
| <span data-ttu-id="a6844-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a6844-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="a6844-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a6844-167">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="a6844-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a6844-168">Range-Lower</span></span>            | <span data-ttu-id="a6844-169">336</span><span class="sxs-lookup"><span data-stu-id="a6844-169">336</span></span>                                                                                                                                   |
| <span data-ttu-id="a6844-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a6844-170">Range-Upper</span></span>            | <span data-ttu-id="a6844-171">336</span><span class="sxs-lookup"><span data-stu-id="a6844-171">336</span></span>                                                                                                                                   |
| <span data-ttu-id="a6844-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a6844-172">Search-Flags</span></span>           | <span data-ttu-id="a6844-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a6844-173">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="a6844-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a6844-174">System-Flags</span></span>           | <span data-ttu-id="a6844-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a6844-175">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="a6844-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a6844-176">Classes used in</span></span>        | [<span data-ttu-id="a6844-177">**MS-DFSR-telereplication**</span><span class="sxs-lookup"><span data-stu-id="a6844-177">**ms-DFSR-ReplicationGroup**</span></span>](c-msdfsr-replicationgroup.md)<br/> [<span data-ttu-id="a6844-178">**MS-DFSR-Connection**</span><span class="sxs-lookup"><span data-stu-id="a6844-178">**ms-DFSR-Connection**</span></span>](c-msdfsr-connection.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a6844-179">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a6844-179">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a6844-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="a6844-180">Entry</span></span> | <span data-ttu-id="a6844-181">Valor</span><span class="sxs-lookup"><span data-stu-id="a6844-181">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6844-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="a6844-182">Link-Id</span></span>                | \-                                                                                                                                    |
| <span data-ttu-id="a6844-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a6844-183">MAPI-Id</span></span>                | \-                                                                                                                                    |
| <span data-ttu-id="a6844-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="a6844-184">System-Only</span></span>            | <span data-ttu-id="a6844-185">Falso</span><span class="sxs-lookup"><span data-stu-id="a6844-185">False</span></span>                                                                                                                                 |
| <span data-ttu-id="a6844-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a6844-186">Is-Single-Valued</span></span>       | <span data-ttu-id="a6844-187">True</span><span class="sxs-lookup"><span data-stu-id="a6844-187">True</span></span>                                                                                                                                  |
| <span data-ttu-id="a6844-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="a6844-188">Is Indexed</span></span>             | <span data-ttu-id="a6844-189">Falso</span><span class="sxs-lookup"><span data-stu-id="a6844-189">False</span></span>                                                                                                                                 |
| <span data-ttu-id="a6844-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a6844-190">In Global Catalog</span></span>      | <span data-ttu-id="a6844-191">Falso</span><span class="sxs-lookup"><span data-stu-id="a6844-191">False</span></span>                                                                                                                                 |
| <span data-ttu-id="a6844-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a6844-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="a6844-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a6844-193">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="a6844-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a6844-194">Range-Lower</span></span>            | <span data-ttu-id="a6844-195">336</span><span class="sxs-lookup"><span data-stu-id="a6844-195">336</span></span>                                                                                                                                   |
| <span data-ttu-id="a6844-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a6844-196">Range-Upper</span></span>            | <span data-ttu-id="a6844-197">336</span><span class="sxs-lookup"><span data-stu-id="a6844-197">336</span></span>                                                                                                                                   |
| <span data-ttu-id="a6844-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a6844-198">Search-Flags</span></span>           | <span data-ttu-id="a6844-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a6844-199">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="a6844-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a6844-200">System-Flags</span></span>           | <span data-ttu-id="a6844-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a6844-201">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="a6844-202">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a6844-202">Classes used in</span></span>        | [<span data-ttu-id="a6844-203">**MS-DFSR-telereplication**</span><span class="sxs-lookup"><span data-stu-id="a6844-203">**ms-DFSR-ReplicationGroup**</span></span>](c-msdfsr-replicationgroup.md)<br/> [<span data-ttu-id="a6844-204">**MS-DFSR-Connection**</span><span class="sxs-lookup"><span data-stu-id="a6844-204">**ms-DFSR-Connection**</span></span>](c-msdfsr-connection.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a6844-205">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a6844-205">Windows Server 2012</span></span>



| <span data-ttu-id="a6844-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="a6844-206">Entry</span></span> | <span data-ttu-id="a6844-207">Valor</span><span class="sxs-lookup"><span data-stu-id="a6844-207">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6844-208">ID do link</span><span class="sxs-lookup"><span data-stu-id="a6844-208">Link-Id</span></span>                | \-                                                                                                                                    |
| <span data-ttu-id="a6844-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a6844-209">MAPI-Id</span></span>                | \-                                                                                                                                    |
| <span data-ttu-id="a6844-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="a6844-210">System-Only</span></span>            | <span data-ttu-id="a6844-211">Falso</span><span class="sxs-lookup"><span data-stu-id="a6844-211">False</span></span>                                                                                                                                 |
| <span data-ttu-id="a6844-212">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a6844-212">Is-Single-Valued</span></span>       | <span data-ttu-id="a6844-213">True</span><span class="sxs-lookup"><span data-stu-id="a6844-213">True</span></span>                                                                                                                                  |
| <span data-ttu-id="a6844-214">É indexado</span><span class="sxs-lookup"><span data-stu-id="a6844-214">Is Indexed</span></span>             | <span data-ttu-id="a6844-215">Falso</span><span class="sxs-lookup"><span data-stu-id="a6844-215">False</span></span>                                                                                                                                 |
| <span data-ttu-id="a6844-216">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a6844-216">In Global Catalog</span></span>      | <span data-ttu-id="a6844-217">Falso</span><span class="sxs-lookup"><span data-stu-id="a6844-217">False</span></span>                                                                                                                                 |
| <span data-ttu-id="a6844-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a6844-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="a6844-219">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a6844-219">O:BAG:BAD:S:</span></span>                                                                                                                          |
| <span data-ttu-id="a6844-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a6844-220">Range-Lower</span></span>            | <span data-ttu-id="a6844-221">336</span><span class="sxs-lookup"><span data-stu-id="a6844-221">336</span></span>                                                                                                                                   |
| <span data-ttu-id="a6844-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a6844-222">Range-Upper</span></span>            | <span data-ttu-id="a6844-223">336</span><span class="sxs-lookup"><span data-stu-id="a6844-223">336</span></span>                                                                                                                                   |
| <span data-ttu-id="a6844-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a6844-224">Search-Flags</span></span>           | <span data-ttu-id="a6844-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a6844-225">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="a6844-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a6844-226">System-Flags</span></span>           | <span data-ttu-id="a6844-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a6844-227">0x00000000</span></span>                                                                                                                            |
| <span data-ttu-id="a6844-228">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a6844-228">Classes used in</span></span>        | [<span data-ttu-id="a6844-229">**MS-DFSR-telereplication**</span><span class="sxs-lookup"><span data-stu-id="a6844-229">**ms-DFSR-ReplicationGroup**</span></span>](c-msdfsr-replicationgroup.md)<br/> [<span data-ttu-id="a6844-230">**MS-DFSR-Connection**</span><span class="sxs-lookup"><span data-stu-id="a6844-230">**ms-DFSR-Connection**</span></span>](c-msdfsr-connection.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="a6844-231">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6844-231">Remarks</span></span>

<span data-ttu-id="a6844-232">O atributo faz parte do suporte ao serviço de replicação do Sistema de Arquivos Distribuído (DFS).</span><span class="sxs-lookup"><span data-stu-id="a6844-232">The attribute is a part of the Distributed File System (DFS) Replication service support.</span></span>

 

 





