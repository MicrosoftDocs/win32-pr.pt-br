---
title: Atributo FRS-File-Filter
description: Uma lista de extensões de nome de arquivo excluídas da replicação de arquivo.
ms.assetid: 094a393a-9e1a-4da8-a38a-161102f164fd
ms.tgt_platform: multiple
keywords:
- FRS-arquivo-filtro de atributo do AD esquema
- Esquema de AD do atributo fRSFileFilter
topic_type:
- apiref
api_name:
- FRS-File-Filter
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 234cf7d6e56e84c2ed9578fc56036e581a2f0ad2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105752977"
---
# <a name="frs-file-filter-attribute"></a><span data-ttu-id="a07a9-105">Atributo FRS-File-Filter</span><span class="sxs-lookup"><span data-stu-id="a07a9-105">FRS-File-Filter attribute</span></span>

<span data-ttu-id="a07a9-106">Uma lista de extensões de nome de arquivo excluídas da replicação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="a07a9-106">A list of file name extensions excluded from file replication.</span></span>



| <span data-ttu-id="a07a9-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="a07a9-107">Entry</span></span> | <span data-ttu-id="a07a9-108">Valor</span><span class="sxs-lookup"><span data-stu-id="a07a9-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="a07a9-109">CN</span><span class="sxs-lookup"><span data-stu-id="a07a9-109">CN</span></span>                | <span data-ttu-id="a07a9-110">FRS-filtro de arquivo</span><span class="sxs-lookup"><span data-stu-id="a07a9-110">FRS-File-Filter</span></span>                             |
| <span data-ttu-id="a07a9-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a07a9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a07a9-112">fRSFileFilter</span><span class="sxs-lookup"><span data-stu-id="a07a9-112">fRSFileFilter</span></span>                               |
| <span data-ttu-id="a07a9-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="a07a9-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="a07a9-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="a07a9-114">Update Privilege</span></span>  | <span data-ttu-id="a07a9-115">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="a07a9-115">Domain administrator</span></span>                        |
| <span data-ttu-id="a07a9-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="a07a9-116">Update Frequency</span></span>  | <span data-ttu-id="a07a9-117">Quando a replicação é configurada.</span><span class="sxs-lookup"><span data-stu-id="a07a9-117">When replication is setup.</span></span>                  |
| <span data-ttu-id="a07a9-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a07a9-118">Attribute-Id</span></span>      | <span data-ttu-id="a07a9-119">1.2.840.113556.1.4.483</span><span class="sxs-lookup"><span data-stu-id="a07a9-119">1.2.840.113556.1.4.483</span></span>                      |
| <span data-ttu-id="a07a9-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a07a9-120">System-Id-Guid</span></span>    | <span data-ttu-id="a07a9-121">1be8f170-a9ff-11d0-afe2-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="a07a9-121">1be8f170-a9ff-11d0-afe2-00c04fd930c9</span></span>        |
| <span data-ttu-id="a07a9-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="a07a9-122">Syntax</span></span>            | [<span data-ttu-id="a07a9-123">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="a07a9-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="a07a9-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="a07a9-124">Implementations</span></span>

-   [<span data-ttu-id="a07a9-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a07a9-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a07a9-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a07a9-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a07a9-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a07a9-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a07a9-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a07a9-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a07a9-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a07a9-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a07a9-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a07a9-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a07a9-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a07a9-131">Windows 2000 Server</span></span>



| <span data-ttu-id="a07a9-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="a07a9-132">Entry</span></span> | <span data-ttu-id="a07a9-133">Valor</span><span class="sxs-lookup"><span data-stu-id="a07a9-133">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="a07a9-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="a07a9-134">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a07a9-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a07a9-135">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a07a9-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="a07a9-136">System-Only</span></span>            | <span data-ttu-id="a07a9-137">Falso</span><span class="sxs-lookup"><span data-stu-id="a07a9-137">False</span></span>                                                     |
| <span data-ttu-id="a07a9-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a07a9-138">Is-Single-Valued</span></span>       | <span data-ttu-id="a07a9-139">True</span><span class="sxs-lookup"><span data-stu-id="a07a9-139">True</span></span>                                                      |
| <span data-ttu-id="a07a9-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="a07a9-140">Is Indexed</span></span>             | <span data-ttu-id="a07a9-141">Falso</span><span class="sxs-lookup"><span data-stu-id="a07a9-141">False</span></span>                                                     |
| <span data-ttu-id="a07a9-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a07a9-142">In Global Catalog</span></span>      | <span data-ttu-id="a07a9-143">Falso</span><span class="sxs-lookup"><span data-stu-id="a07a9-143">False</span></span>                                                     |
| <span data-ttu-id="a07a9-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a07a9-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="a07a9-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a07a9-145">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="a07a9-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a07a9-146">Range-Lower</span></span>            | <span data-ttu-id="a07a9-147">0</span><span class="sxs-lookup"><span data-stu-id="a07a9-147">0</span></span>                                                         |
| <span data-ttu-id="a07a9-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a07a9-148">Range-Upper</span></span>            | <span data-ttu-id="a07a9-149">2.048</span><span class="sxs-lookup"><span data-stu-id="a07a9-149">2048</span></span>                                                      |
| <span data-ttu-id="a07a9-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a07a9-150">Search-Flags</span></span>           | <span data-ttu-id="a07a9-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a07a9-151">0x00000000</span></span>                                                |
| <span data-ttu-id="a07a9-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a07a9-152">System-Flags</span></span>           | <span data-ttu-id="a07a9-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a07a9-153">0x00000010</span></span>                                                |
| <span data-ttu-id="a07a9-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a07a9-154">Classes used in</span></span>        | [<span data-ttu-id="a07a9-155">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="a07a9-155">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a07a9-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a07a9-156">Windows Server 2003</span></span>



| <span data-ttu-id="a07a9-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="a07a9-157">Entry</span></span> | <span data-ttu-id="a07a9-158">Valor</span><span class="sxs-lookup"><span data-stu-id="a07a9-158">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="a07a9-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="a07a9-159">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a07a9-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a07a9-160">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a07a9-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="a07a9-161">System-Only</span></span>            | <span data-ttu-id="a07a9-162">Falso</span><span class="sxs-lookup"><span data-stu-id="a07a9-162">False</span></span>                                                     |
| <span data-ttu-id="a07a9-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a07a9-163">Is-Single-Valued</span></span>       | <span data-ttu-id="a07a9-164">True</span><span class="sxs-lookup"><span data-stu-id="a07a9-164">True</span></span>                                                      |
| <span data-ttu-id="a07a9-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="a07a9-165">Is Indexed</span></span>             | <span data-ttu-id="a07a9-166">Falso</span><span class="sxs-lookup"><span data-stu-id="a07a9-166">False</span></span>                                                     |
| <span data-ttu-id="a07a9-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a07a9-167">In Global Catalog</span></span>      | <span data-ttu-id="a07a9-168">Falso</span><span class="sxs-lookup"><span data-stu-id="a07a9-168">False</span></span>                                                     |
| <span data-ttu-id="a07a9-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a07a9-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="a07a9-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a07a9-170">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="a07a9-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a07a9-171">Range-Lower</span></span>            | <span data-ttu-id="a07a9-172">0</span><span class="sxs-lookup"><span data-stu-id="a07a9-172">0</span></span>                                                         |
| <span data-ttu-id="a07a9-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a07a9-173">Range-Upper</span></span>            | <span data-ttu-id="a07a9-174">2.048</span><span class="sxs-lookup"><span data-stu-id="a07a9-174">2048</span></span>                                                      |
| <span data-ttu-id="a07a9-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a07a9-175">Search-Flags</span></span>           | <span data-ttu-id="a07a9-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a07a9-176">0x00000000</span></span>                                                |
| <span data-ttu-id="a07a9-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a07a9-177">System-Flags</span></span>           | <span data-ttu-id="a07a9-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a07a9-178">0x00000010</span></span>                                                |
| <span data-ttu-id="a07a9-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a07a9-179">Classes used in</span></span>        | [<span data-ttu-id="a07a9-180">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="a07a9-180">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a07a9-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a07a9-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a07a9-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="a07a9-182">Entry</span></span> | <span data-ttu-id="a07a9-183">Valor</span><span class="sxs-lookup"><span data-stu-id="a07a9-183">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="a07a9-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="a07a9-184">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a07a9-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a07a9-185">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a07a9-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="a07a9-186">System-Only</span></span>            | <span data-ttu-id="a07a9-187">Falso</span><span class="sxs-lookup"><span data-stu-id="a07a9-187">False</span></span>                                                     |
| <span data-ttu-id="a07a9-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a07a9-188">Is-Single-Valued</span></span>       | <span data-ttu-id="a07a9-189">True</span><span class="sxs-lookup"><span data-stu-id="a07a9-189">True</span></span>                                                      |
| <span data-ttu-id="a07a9-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="a07a9-190">Is Indexed</span></span>             | <span data-ttu-id="a07a9-191">Falso</span><span class="sxs-lookup"><span data-stu-id="a07a9-191">False</span></span>                                                     |
| <span data-ttu-id="a07a9-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a07a9-192">In Global Catalog</span></span>      | <span data-ttu-id="a07a9-193">Falso</span><span class="sxs-lookup"><span data-stu-id="a07a9-193">False</span></span>                                                     |
| <span data-ttu-id="a07a9-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a07a9-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="a07a9-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a07a9-195">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="a07a9-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a07a9-196">Range-Lower</span></span>            | <span data-ttu-id="a07a9-197">0</span><span class="sxs-lookup"><span data-stu-id="a07a9-197">0</span></span>                                                         |
| <span data-ttu-id="a07a9-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a07a9-198">Range-Upper</span></span>            | <span data-ttu-id="a07a9-199">2.048</span><span class="sxs-lookup"><span data-stu-id="a07a9-199">2048</span></span>                                                      |
| <span data-ttu-id="a07a9-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a07a9-200">Search-Flags</span></span>           | <span data-ttu-id="a07a9-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a07a9-201">0x00000000</span></span>                                                |
| <span data-ttu-id="a07a9-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a07a9-202">System-Flags</span></span>           | <span data-ttu-id="a07a9-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a07a9-203">0x00000010</span></span>                                                |
| <span data-ttu-id="a07a9-204">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a07a9-204">Classes used in</span></span>        | [<span data-ttu-id="a07a9-205">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="a07a9-205">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a07a9-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a07a9-206">Windows Server 2008</span></span>



| <span data-ttu-id="a07a9-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="a07a9-207">Entry</span></span> | <span data-ttu-id="a07a9-208">Valor</span><span class="sxs-lookup"><span data-stu-id="a07a9-208">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="a07a9-209">ID do link</span><span class="sxs-lookup"><span data-stu-id="a07a9-209">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a07a9-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a07a9-210">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a07a9-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="a07a9-211">System-Only</span></span>            | <span data-ttu-id="a07a9-212">Falso</span><span class="sxs-lookup"><span data-stu-id="a07a9-212">False</span></span>                                                     |
| <span data-ttu-id="a07a9-213">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a07a9-213">Is-Single-Valued</span></span>       | <span data-ttu-id="a07a9-214">True</span><span class="sxs-lookup"><span data-stu-id="a07a9-214">True</span></span>                                                      |
| <span data-ttu-id="a07a9-215">É indexado</span><span class="sxs-lookup"><span data-stu-id="a07a9-215">Is Indexed</span></span>             | <span data-ttu-id="a07a9-216">Falso</span><span class="sxs-lookup"><span data-stu-id="a07a9-216">False</span></span>                                                     |
| <span data-ttu-id="a07a9-217">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a07a9-217">In Global Catalog</span></span>      | <span data-ttu-id="a07a9-218">Falso</span><span class="sxs-lookup"><span data-stu-id="a07a9-218">False</span></span>                                                     |
| <span data-ttu-id="a07a9-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a07a9-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="a07a9-220">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a07a9-220">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="a07a9-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a07a9-221">Range-Lower</span></span>            | <span data-ttu-id="a07a9-222">0</span><span class="sxs-lookup"><span data-stu-id="a07a9-222">0</span></span>                                                         |
| <span data-ttu-id="a07a9-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a07a9-223">Range-Upper</span></span>            | <span data-ttu-id="a07a9-224">2.048</span><span class="sxs-lookup"><span data-stu-id="a07a9-224">2048</span></span>                                                      |
| <span data-ttu-id="a07a9-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a07a9-225">Search-Flags</span></span>           | <span data-ttu-id="a07a9-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a07a9-226">0x00000000</span></span>                                                |
| <span data-ttu-id="a07a9-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a07a9-227">System-Flags</span></span>           | <span data-ttu-id="a07a9-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a07a9-228">0x00000010</span></span>                                                |
| <span data-ttu-id="a07a9-229">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a07a9-229">Classes used in</span></span>        | [<span data-ttu-id="a07a9-230">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="a07a9-230">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a07a9-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a07a9-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a07a9-232">Entrada</span><span class="sxs-lookup"><span data-stu-id="a07a9-232">Entry</span></span> | <span data-ttu-id="a07a9-233">Valor</span><span class="sxs-lookup"><span data-stu-id="a07a9-233">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="a07a9-234">ID do link</span><span class="sxs-lookup"><span data-stu-id="a07a9-234">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a07a9-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a07a9-235">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a07a9-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="a07a9-236">System-Only</span></span>            | <span data-ttu-id="a07a9-237">Falso</span><span class="sxs-lookup"><span data-stu-id="a07a9-237">False</span></span>                                                     |
| <span data-ttu-id="a07a9-238">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a07a9-238">Is-Single-Valued</span></span>       | <span data-ttu-id="a07a9-239">True</span><span class="sxs-lookup"><span data-stu-id="a07a9-239">True</span></span>                                                      |
| <span data-ttu-id="a07a9-240">É indexado</span><span class="sxs-lookup"><span data-stu-id="a07a9-240">Is Indexed</span></span>             | <span data-ttu-id="a07a9-241">Falso</span><span class="sxs-lookup"><span data-stu-id="a07a9-241">False</span></span>                                                     |
| <span data-ttu-id="a07a9-242">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a07a9-242">In Global Catalog</span></span>      | <span data-ttu-id="a07a9-243">Falso</span><span class="sxs-lookup"><span data-stu-id="a07a9-243">False</span></span>                                                     |
| <span data-ttu-id="a07a9-244">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a07a9-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="a07a9-245">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a07a9-245">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="a07a9-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a07a9-246">Range-Lower</span></span>            | <span data-ttu-id="a07a9-247">0</span><span class="sxs-lookup"><span data-stu-id="a07a9-247">0</span></span>                                                         |
| <span data-ttu-id="a07a9-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a07a9-248">Range-Upper</span></span>            | <span data-ttu-id="a07a9-249">2.048</span><span class="sxs-lookup"><span data-stu-id="a07a9-249">2048</span></span>                                                      |
| <span data-ttu-id="a07a9-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a07a9-250">Search-Flags</span></span>           | <span data-ttu-id="a07a9-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a07a9-251">0x00000000</span></span>                                                |
| <span data-ttu-id="a07a9-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a07a9-252">System-Flags</span></span>           | <span data-ttu-id="a07a9-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a07a9-253">0x00000010</span></span>                                                |
| <span data-ttu-id="a07a9-254">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a07a9-254">Classes used in</span></span>        | [<span data-ttu-id="a07a9-255">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="a07a9-255">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a07a9-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a07a9-256">Windows Server 2012</span></span>



| <span data-ttu-id="a07a9-257">Entrada</span><span class="sxs-lookup"><span data-stu-id="a07a9-257">Entry</span></span> | <span data-ttu-id="a07a9-258">Valor</span><span class="sxs-lookup"><span data-stu-id="a07a9-258">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="a07a9-259">ID do link</span><span class="sxs-lookup"><span data-stu-id="a07a9-259">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a07a9-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a07a9-260">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a07a9-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="a07a9-261">System-Only</span></span>            | <span data-ttu-id="a07a9-262">Falso</span><span class="sxs-lookup"><span data-stu-id="a07a9-262">False</span></span>                                                     |
| <span data-ttu-id="a07a9-263">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a07a9-263">Is-Single-Valued</span></span>       | <span data-ttu-id="a07a9-264">True</span><span class="sxs-lookup"><span data-stu-id="a07a9-264">True</span></span>                                                      |
| <span data-ttu-id="a07a9-265">É indexado</span><span class="sxs-lookup"><span data-stu-id="a07a9-265">Is Indexed</span></span>             | <span data-ttu-id="a07a9-266">Falso</span><span class="sxs-lookup"><span data-stu-id="a07a9-266">False</span></span>                                                     |
| <span data-ttu-id="a07a9-267">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a07a9-267">In Global Catalog</span></span>      | <span data-ttu-id="a07a9-268">Falso</span><span class="sxs-lookup"><span data-stu-id="a07a9-268">False</span></span>                                                     |
| <span data-ttu-id="a07a9-269">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a07a9-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="a07a9-270">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a07a9-270">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="a07a9-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a07a9-271">Range-Lower</span></span>            | <span data-ttu-id="a07a9-272">0</span><span class="sxs-lookup"><span data-stu-id="a07a9-272">0</span></span>                                                         |
| <span data-ttu-id="a07a9-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a07a9-273">Range-Upper</span></span>            | <span data-ttu-id="a07a9-274">2.048</span><span class="sxs-lookup"><span data-stu-id="a07a9-274">2048</span></span>                                                      |
| <span data-ttu-id="a07a9-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a07a9-275">Search-Flags</span></span>           | <span data-ttu-id="a07a9-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a07a9-276">0x00000000</span></span>                                                |
| <span data-ttu-id="a07a9-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a07a9-277">System-Flags</span></span>           | <span data-ttu-id="a07a9-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a07a9-278">0x00000010</span></span>                                                |
| <span data-ttu-id="a07a9-279">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a07a9-279">Classes used in</span></span>        | [<span data-ttu-id="a07a9-280">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="a07a9-280">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





