---
title: FRS-raiz-atributo de segurança
description: O descritor de segurança da raiz do conjunto de réplicas para replicação de arquivo.
ms.assetid: 1db92f68-465a-4d93-ad4d-706ef4761ddc
ms.tgt_platform: multiple
keywords:
- FRS-raiz-atributo de segurança esquema do AD
- Esquema de AD do atributo fRSRootSecurity
topic_type:
- apiref
api_name:
- FRS-Root-Security
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a84059902998b120ad38215257fdddcb1c21ea6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105748334"
---
# <a name="frs-root-security-attribute"></a><span data-ttu-id="0c269-105">FRS-raiz-atributo de segurança</span><span class="sxs-lookup"><span data-stu-id="0c269-105">FRS-Root-Security attribute</span></span>

<span data-ttu-id="0c269-106">O descritor de segurança da raiz do conjunto de réplicas para replicação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="0c269-106">The security descriptor of replica set root for file replication.</span></span>



| <span data-ttu-id="0c269-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="0c269-107">Entry</span></span> | <span data-ttu-id="0c269-108">Valor</span><span class="sxs-lookup"><span data-stu-id="0c269-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="0c269-109">CN</span><span class="sxs-lookup"><span data-stu-id="0c269-109">CN</span></span>                | <span data-ttu-id="0c269-110">FRS-raiz-segurança</span><span class="sxs-lookup"><span data-stu-id="0c269-110">FRS-Root-Security</span></span>                                   |
| <span data-ttu-id="0c269-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0c269-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0c269-112">fRSRootSecurity</span><span class="sxs-lookup"><span data-stu-id="0c269-112">fRSRootSecurity</span></span>                                     |
| <span data-ttu-id="0c269-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="0c269-113">Size</span></span>              | \-                                                  |
| <span data-ttu-id="0c269-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="0c269-114">Update Privilege</span></span>  | \-                                                  |
| <span data-ttu-id="0c269-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="0c269-115">Update Frequency</span></span>  | \-                                                  |
| <span data-ttu-id="0c269-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0c269-116">Attribute-Id</span></span>      | <span data-ttu-id="0c269-117">1.2.840.113556.1.4.535</span><span class="sxs-lookup"><span data-stu-id="0c269-117">1.2.840.113556.1.4.535</span></span>                              |
| <span data-ttu-id="0c269-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0c269-118">System-Id-Guid</span></span>    | <span data-ttu-id="0c269-119">5245801f-ca6a-11d0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="0c269-119">5245801f-ca6a-11d0-afff-0000f80367c1</span></span>                |
| <span data-ttu-id="0c269-120">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0c269-120">Syntax</span></span>            | [<span data-ttu-id="0c269-121">**Cadeia de caracteres (NT-SEC-DESC)**</span><span class="sxs-lookup"><span data-stu-id="0c269-121">**String(NT-Sec-Desc)**</span></span>](s-string-nt-sec-desc.md) |



## <a name="implementations"></a><span data-ttu-id="0c269-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="0c269-122">Implementations</span></span>

-   [<span data-ttu-id="0c269-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0c269-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0c269-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0c269-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0c269-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0c269-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0c269-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0c269-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0c269-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0c269-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0c269-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0c269-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0c269-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0c269-129">Windows 2000 Server</span></span>



| <span data-ttu-id="0c269-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="0c269-130">Entry</span></span> | <span data-ttu-id="0c269-131">Valor</span><span class="sxs-lookup"><span data-stu-id="0c269-131">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c269-132">ID do link</span><span class="sxs-lookup"><span data-stu-id="0c269-132">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="0c269-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c269-133">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="0c269-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c269-134">System-Only</span></span>            | <span data-ttu-id="0c269-135">Falso</span><span class="sxs-lookup"><span data-stu-id="0c269-135">False</span></span>                                                                                                      |
| <span data-ttu-id="0c269-136">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0c269-136">Is-Single-Valued</span></span>       | <span data-ttu-id="0c269-137">True</span><span class="sxs-lookup"><span data-stu-id="0c269-137">True</span></span>                                                                                                       |
| <span data-ttu-id="0c269-138">É indexado</span><span class="sxs-lookup"><span data-stu-id="0c269-138">Is Indexed</span></span>             | <span data-ttu-id="0c269-139">Falso</span><span class="sxs-lookup"><span data-stu-id="0c269-139">False</span></span>                                                                                                      |
| <span data-ttu-id="0c269-140">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0c269-140">In Global Catalog</span></span>      | <span data-ttu-id="0c269-141">Falso</span><span class="sxs-lookup"><span data-stu-id="0c269-141">False</span></span>                                                                                                      |
| <span data-ttu-id="0c269-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0c269-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c269-143">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0c269-143">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="0c269-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c269-144">Range-Lower</span></span>            | <span data-ttu-id="0c269-145">0</span><span class="sxs-lookup"><span data-stu-id="0c269-145">0</span></span>                                                                                                          |
| <span data-ttu-id="0c269-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c269-146">Range-Upper</span></span>            | <span data-ttu-id="0c269-147">65535</span><span class="sxs-lookup"><span data-stu-id="0c269-147">65535</span></span>                                                                                                      |
| <span data-ttu-id="0c269-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c269-148">Search-Flags</span></span>           | <span data-ttu-id="0c269-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c269-149">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="0c269-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c269-150">System-Flags</span></span>           | <span data-ttu-id="0c269-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c269-151">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="0c269-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0c269-152">Classes used in</span></span>        | [<span data-ttu-id="0c269-153">**NTFRS-membro**</span><span class="sxs-lookup"><span data-stu-id="0c269-153">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="0c269-154">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="0c269-154">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0c269-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0c269-155">Windows Server 2003</span></span>



| <span data-ttu-id="0c269-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="0c269-156">Entry</span></span> | <span data-ttu-id="0c269-157">Valor</span><span class="sxs-lookup"><span data-stu-id="0c269-157">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c269-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="0c269-158">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="0c269-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c269-159">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="0c269-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c269-160">System-Only</span></span>            | <span data-ttu-id="0c269-161">Falso</span><span class="sxs-lookup"><span data-stu-id="0c269-161">False</span></span>                                                                                                      |
| <span data-ttu-id="0c269-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0c269-162">Is-Single-Valued</span></span>       | <span data-ttu-id="0c269-163">True</span><span class="sxs-lookup"><span data-stu-id="0c269-163">True</span></span>                                                                                                       |
| <span data-ttu-id="0c269-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="0c269-164">Is Indexed</span></span>             | <span data-ttu-id="0c269-165">Falso</span><span class="sxs-lookup"><span data-stu-id="0c269-165">False</span></span>                                                                                                      |
| <span data-ttu-id="0c269-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0c269-166">In Global Catalog</span></span>      | <span data-ttu-id="0c269-167">Falso</span><span class="sxs-lookup"><span data-stu-id="0c269-167">False</span></span>                                                                                                      |
| <span data-ttu-id="0c269-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0c269-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c269-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0c269-169">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="0c269-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c269-170">Range-Lower</span></span>            | <span data-ttu-id="0c269-171">0</span><span class="sxs-lookup"><span data-stu-id="0c269-171">0</span></span>                                                                                                          |
| <span data-ttu-id="0c269-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c269-172">Range-Upper</span></span>            | <span data-ttu-id="0c269-173">65535</span><span class="sxs-lookup"><span data-stu-id="0c269-173">65535</span></span>                                                                                                      |
| <span data-ttu-id="0c269-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c269-174">Search-Flags</span></span>           | <span data-ttu-id="0c269-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c269-175">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="0c269-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c269-176">System-Flags</span></span>           | <span data-ttu-id="0c269-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c269-177">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="0c269-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0c269-178">Classes used in</span></span>        | [<span data-ttu-id="0c269-179">**NTFRS-membro**</span><span class="sxs-lookup"><span data-stu-id="0c269-179">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="0c269-180">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="0c269-180">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0c269-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0c269-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0c269-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="0c269-182">Entry</span></span> | <span data-ttu-id="0c269-183">Valor</span><span class="sxs-lookup"><span data-stu-id="0c269-183">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c269-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="0c269-184">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="0c269-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c269-185">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="0c269-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c269-186">System-Only</span></span>            | <span data-ttu-id="0c269-187">Falso</span><span class="sxs-lookup"><span data-stu-id="0c269-187">False</span></span>                                                                                                      |
| <span data-ttu-id="0c269-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0c269-188">Is-Single-Valued</span></span>       | <span data-ttu-id="0c269-189">True</span><span class="sxs-lookup"><span data-stu-id="0c269-189">True</span></span>                                                                                                       |
| <span data-ttu-id="0c269-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="0c269-190">Is Indexed</span></span>             | <span data-ttu-id="0c269-191">Falso</span><span class="sxs-lookup"><span data-stu-id="0c269-191">False</span></span>                                                                                                      |
| <span data-ttu-id="0c269-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0c269-192">In Global Catalog</span></span>      | <span data-ttu-id="0c269-193">Falso</span><span class="sxs-lookup"><span data-stu-id="0c269-193">False</span></span>                                                                                                      |
| <span data-ttu-id="0c269-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0c269-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c269-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0c269-195">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="0c269-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c269-196">Range-Lower</span></span>            | <span data-ttu-id="0c269-197">0</span><span class="sxs-lookup"><span data-stu-id="0c269-197">0</span></span>                                                                                                          |
| <span data-ttu-id="0c269-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c269-198">Range-Upper</span></span>            | <span data-ttu-id="0c269-199">65535</span><span class="sxs-lookup"><span data-stu-id="0c269-199">65535</span></span>                                                                                                      |
| <span data-ttu-id="0c269-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c269-200">Search-Flags</span></span>           | <span data-ttu-id="0c269-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c269-201">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="0c269-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c269-202">System-Flags</span></span>           | <span data-ttu-id="0c269-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c269-203">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="0c269-204">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0c269-204">Classes used in</span></span>        | [<span data-ttu-id="0c269-205">**NTFRS-membro**</span><span class="sxs-lookup"><span data-stu-id="0c269-205">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="0c269-206">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="0c269-206">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0c269-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c269-207">Windows Server 2008</span></span>



| <span data-ttu-id="0c269-208">Entrada</span><span class="sxs-lookup"><span data-stu-id="0c269-208">Entry</span></span> | <span data-ttu-id="0c269-209">Valor</span><span class="sxs-lookup"><span data-stu-id="0c269-209">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c269-210">ID do link</span><span class="sxs-lookup"><span data-stu-id="0c269-210">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="0c269-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c269-211">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="0c269-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c269-212">System-Only</span></span>            | <span data-ttu-id="0c269-213">Falso</span><span class="sxs-lookup"><span data-stu-id="0c269-213">False</span></span>                                                                                                      |
| <span data-ttu-id="0c269-214">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0c269-214">Is-Single-Valued</span></span>       | <span data-ttu-id="0c269-215">True</span><span class="sxs-lookup"><span data-stu-id="0c269-215">True</span></span>                                                                                                       |
| <span data-ttu-id="0c269-216">É indexado</span><span class="sxs-lookup"><span data-stu-id="0c269-216">Is Indexed</span></span>             | <span data-ttu-id="0c269-217">Falso</span><span class="sxs-lookup"><span data-stu-id="0c269-217">False</span></span>                                                                                                      |
| <span data-ttu-id="0c269-218">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0c269-218">In Global Catalog</span></span>      | <span data-ttu-id="0c269-219">Falso</span><span class="sxs-lookup"><span data-stu-id="0c269-219">False</span></span>                                                                                                      |
| <span data-ttu-id="0c269-220">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0c269-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c269-221">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0c269-221">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="0c269-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c269-222">Range-Lower</span></span>            | <span data-ttu-id="0c269-223">0</span><span class="sxs-lookup"><span data-stu-id="0c269-223">0</span></span>                                                                                                          |
| <span data-ttu-id="0c269-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c269-224">Range-Upper</span></span>            | <span data-ttu-id="0c269-225">65535</span><span class="sxs-lookup"><span data-stu-id="0c269-225">65535</span></span>                                                                                                      |
| <span data-ttu-id="0c269-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c269-226">Search-Flags</span></span>           | <span data-ttu-id="0c269-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c269-227">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="0c269-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c269-228">System-Flags</span></span>           | <span data-ttu-id="0c269-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c269-229">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="0c269-230">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0c269-230">Classes used in</span></span>        | [<span data-ttu-id="0c269-231">**NTFRS-membro**</span><span class="sxs-lookup"><span data-stu-id="0c269-231">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="0c269-232">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="0c269-232">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0c269-233">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0c269-233">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0c269-234">Entrada</span><span class="sxs-lookup"><span data-stu-id="0c269-234">Entry</span></span> | <span data-ttu-id="0c269-235">Valor</span><span class="sxs-lookup"><span data-stu-id="0c269-235">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c269-236">ID do link</span><span class="sxs-lookup"><span data-stu-id="0c269-236">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="0c269-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c269-237">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="0c269-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c269-238">System-Only</span></span>            | <span data-ttu-id="0c269-239">Falso</span><span class="sxs-lookup"><span data-stu-id="0c269-239">False</span></span>                                                                                                      |
| <span data-ttu-id="0c269-240">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0c269-240">Is-Single-Valued</span></span>       | <span data-ttu-id="0c269-241">True</span><span class="sxs-lookup"><span data-stu-id="0c269-241">True</span></span>                                                                                                       |
| <span data-ttu-id="0c269-242">É indexado</span><span class="sxs-lookup"><span data-stu-id="0c269-242">Is Indexed</span></span>             | <span data-ttu-id="0c269-243">Falso</span><span class="sxs-lookup"><span data-stu-id="0c269-243">False</span></span>                                                                                                      |
| <span data-ttu-id="0c269-244">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0c269-244">In Global Catalog</span></span>      | <span data-ttu-id="0c269-245">Falso</span><span class="sxs-lookup"><span data-stu-id="0c269-245">False</span></span>                                                                                                      |
| <span data-ttu-id="0c269-246">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0c269-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c269-247">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0c269-247">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="0c269-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c269-248">Range-Lower</span></span>            | <span data-ttu-id="0c269-249">0</span><span class="sxs-lookup"><span data-stu-id="0c269-249">0</span></span>                                                                                                          |
| <span data-ttu-id="0c269-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c269-250">Range-Upper</span></span>            | <span data-ttu-id="0c269-251">65535</span><span class="sxs-lookup"><span data-stu-id="0c269-251">65535</span></span>                                                                                                      |
| <span data-ttu-id="0c269-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c269-252">Search-Flags</span></span>           | <span data-ttu-id="0c269-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c269-253">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="0c269-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c269-254">System-Flags</span></span>           | <span data-ttu-id="0c269-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c269-255">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="0c269-256">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0c269-256">Classes used in</span></span>        | [<span data-ttu-id="0c269-257">**NTFRS-membro**</span><span class="sxs-lookup"><span data-stu-id="0c269-257">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="0c269-258">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="0c269-258">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0c269-259">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0c269-259">Windows Server 2012</span></span>



| <span data-ttu-id="0c269-260">Entrada</span><span class="sxs-lookup"><span data-stu-id="0c269-260">Entry</span></span> | <span data-ttu-id="0c269-261">Valor</span><span class="sxs-lookup"><span data-stu-id="0c269-261">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c269-262">ID do link</span><span class="sxs-lookup"><span data-stu-id="0c269-262">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="0c269-263">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c269-263">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="0c269-264">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c269-264">System-Only</span></span>            | <span data-ttu-id="0c269-265">Falso</span><span class="sxs-lookup"><span data-stu-id="0c269-265">False</span></span>                                                                                                      |
| <span data-ttu-id="0c269-266">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0c269-266">Is-Single-Valued</span></span>       | <span data-ttu-id="0c269-267">True</span><span class="sxs-lookup"><span data-stu-id="0c269-267">True</span></span>                                                                                                       |
| <span data-ttu-id="0c269-268">É indexado</span><span class="sxs-lookup"><span data-stu-id="0c269-268">Is Indexed</span></span>             | <span data-ttu-id="0c269-269">Falso</span><span class="sxs-lookup"><span data-stu-id="0c269-269">False</span></span>                                                                                                      |
| <span data-ttu-id="0c269-270">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0c269-270">In Global Catalog</span></span>      | <span data-ttu-id="0c269-271">Falso</span><span class="sxs-lookup"><span data-stu-id="0c269-271">False</span></span>                                                                                                      |
| <span data-ttu-id="0c269-272">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0c269-272">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c269-273">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0c269-273">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="0c269-274">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c269-274">Range-Lower</span></span>            | <span data-ttu-id="0c269-275">0</span><span class="sxs-lookup"><span data-stu-id="0c269-275">0</span></span>                                                                                                          |
| <span data-ttu-id="0c269-276">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c269-276">Range-Upper</span></span>            | <span data-ttu-id="0c269-277">65535</span><span class="sxs-lookup"><span data-stu-id="0c269-277">65535</span></span>                                                                                                      |
| <span data-ttu-id="0c269-278">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c269-278">Search-Flags</span></span>           | <span data-ttu-id="0c269-279">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0c269-279">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="0c269-280">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c269-280">System-Flags</span></span>           | <span data-ttu-id="0c269-281">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c269-281">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="0c269-282">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0c269-282">Classes used in</span></span>        | [<span data-ttu-id="0c269-283">**NTFRS-membro**</span><span class="sxs-lookup"><span data-stu-id="0c269-283">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="0c269-284">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="0c269-284">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





