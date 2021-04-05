---
title: Último-backup-atributo de tempo de restauração
description: Quando a última restauração do sistema ocorreu.
ms.assetid: 44850c16-3f17-4883-9a54-3e82ca7d63da
ms.tgt_platform: multiple
keywords:
- Último-backup – atributo de tempo de restauração – esquema do AD
- Esquema de AD do atributo lastBackupRestorationTime
topic_type:
- apiref
api_name:
- Last-Backup-Restoration-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9220d06a4cdd562599611d2ad19cf09fa279ef3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104009796"
---
# <a name="last-backup-restoration-time-attribute"></a><span data-ttu-id="26ceb-105">Último-backup-atributo de tempo de restauração</span><span class="sxs-lookup"><span data-stu-id="26ceb-105">Last-Backup-Restoration-Time attribute</span></span>

<span data-ttu-id="26ceb-106">Quando a última restauração do sistema ocorreu.</span><span class="sxs-lookup"><span data-stu-id="26ceb-106">When the last system restore occurred.</span></span>



| <span data-ttu-id="26ceb-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="26ceb-107">Entry</span></span> | <span data-ttu-id="26ceb-108">Valor</span><span class="sxs-lookup"><span data-stu-id="26ceb-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="26ceb-109">CN</span><span class="sxs-lookup"><span data-stu-id="26ceb-109">CN</span></span>                | <span data-ttu-id="26ceb-110">Último backup-tempo de restauração</span><span class="sxs-lookup"><span data-stu-id="26ceb-110">Last-Backup-Restoration-Time</span></span>         |
| <span data-ttu-id="26ceb-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="26ceb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="26ceb-112">lastBackupRestorationTime</span><span class="sxs-lookup"><span data-stu-id="26ceb-112">lastBackupRestorationTime</span></span>            |
| <span data-ttu-id="26ceb-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="26ceb-113">Size</span></span>              | <span data-ttu-id="26ceb-114">8 bytes</span><span class="sxs-lookup"><span data-stu-id="26ceb-114">8 bytes</span></span>                              |
| <span data-ttu-id="26ceb-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="26ceb-115">Update Privilege</span></span>  | <span data-ttu-id="26ceb-116">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="26ceb-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="26ceb-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="26ceb-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="26ceb-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="26ceb-118">Attribute-Id</span></span>      | <span data-ttu-id="26ceb-119">1.2.840.113556.1.4.519</span><span class="sxs-lookup"><span data-stu-id="26ceb-119">1.2.840.113556.1.4.519</span></span>               |
| <span data-ttu-id="26ceb-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="26ceb-120">System-Id-Guid</span></span>    | <span data-ttu-id="26ceb-121">1fbb0be8-ba63-11d0-afef-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="26ceb-121">1fbb0be8-ba63-11d0-afef-0000f80367c1</span></span> |
| <span data-ttu-id="26ceb-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="26ceb-122">Syntax</span></span>            | [<span data-ttu-id="26ceb-123">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="26ceb-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="26ceb-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="26ceb-124">Implementations</span></span>

-   [<span data-ttu-id="26ceb-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="26ceb-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="26ceb-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="26ceb-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="26ceb-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="26ceb-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="26ceb-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="26ceb-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="26ceb-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="26ceb-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="26ceb-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="26ceb-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="26ceb-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="26ceb-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="26ceb-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="26ceb-132">Windows 2000 Server</span></span>



| <span data-ttu-id="26ceb-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="26ceb-133">Entry</span></span> | <span data-ttu-id="26ceb-134">Valor</span><span class="sxs-lookup"><span data-stu-id="26ceb-134">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="26ceb-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="26ceb-135">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="26ceb-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26ceb-136">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="26ceb-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="26ceb-137">System-Only</span></span>            | <span data-ttu-id="26ceb-138">Falso</span><span class="sxs-lookup"><span data-stu-id="26ceb-138">False</span></span>                                    |
| <span data-ttu-id="26ceb-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="26ceb-139">Is-Single-Valued</span></span>       | <span data-ttu-id="26ceb-140">True</span><span class="sxs-lookup"><span data-stu-id="26ceb-140">True</span></span>                                     |
| <span data-ttu-id="26ceb-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="26ceb-141">Is Indexed</span></span>             | <span data-ttu-id="26ceb-142">Falso</span><span class="sxs-lookup"><span data-stu-id="26ceb-142">False</span></span>                                    |
| <span data-ttu-id="26ceb-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="26ceb-143">In Global Catalog</span></span>      | <span data-ttu-id="26ceb-144">Falso</span><span class="sxs-lookup"><span data-stu-id="26ceb-144">False</span></span>                                    |
| <span data-ttu-id="26ceb-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="26ceb-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="26ceb-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="26ceb-146">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="26ceb-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26ceb-147">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="26ceb-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26ceb-148">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="26ceb-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26ceb-149">Search-Flags</span></span>           | <span data-ttu-id="26ceb-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26ceb-150">0x00000000</span></span>                               |
| <span data-ttu-id="26ceb-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26ceb-151">System-Flags</span></span>           | <span data-ttu-id="26ceb-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="26ceb-152">0x00000010</span></span>                               |
| <span data-ttu-id="26ceb-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="26ceb-153">Classes used in</span></span>        | [<span data-ttu-id="26ceb-154">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="26ceb-154">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="26ceb-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="26ceb-155">Windows Server 2003</span></span>



| <span data-ttu-id="26ceb-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="26ceb-156">Entry</span></span> | <span data-ttu-id="26ceb-157">Valor</span><span class="sxs-lookup"><span data-stu-id="26ceb-157">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="26ceb-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="26ceb-158">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="26ceb-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26ceb-159">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="26ceb-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="26ceb-160">System-Only</span></span>            | <span data-ttu-id="26ceb-161">Falso</span><span class="sxs-lookup"><span data-stu-id="26ceb-161">False</span></span>                                    |
| <span data-ttu-id="26ceb-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="26ceb-162">Is-Single-Valued</span></span>       | <span data-ttu-id="26ceb-163">True</span><span class="sxs-lookup"><span data-stu-id="26ceb-163">True</span></span>                                     |
| <span data-ttu-id="26ceb-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="26ceb-164">Is Indexed</span></span>             | <span data-ttu-id="26ceb-165">Falso</span><span class="sxs-lookup"><span data-stu-id="26ceb-165">False</span></span>                                    |
| <span data-ttu-id="26ceb-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="26ceb-166">In Global Catalog</span></span>      | <span data-ttu-id="26ceb-167">Falso</span><span class="sxs-lookup"><span data-stu-id="26ceb-167">False</span></span>                                    |
| <span data-ttu-id="26ceb-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="26ceb-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="26ceb-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="26ceb-169">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="26ceb-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26ceb-170">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="26ceb-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26ceb-171">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="26ceb-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26ceb-172">Search-Flags</span></span>           | <span data-ttu-id="26ceb-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26ceb-173">0x00000000</span></span>                               |
| <span data-ttu-id="26ceb-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26ceb-174">System-Flags</span></span>           | <span data-ttu-id="26ceb-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="26ceb-175">0x00000010</span></span>                               |
| <span data-ttu-id="26ceb-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="26ceb-176">Classes used in</span></span>        | [<span data-ttu-id="26ceb-177">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="26ceb-177">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="26ceb-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="26ceb-178">ADAM</span></span>



| <span data-ttu-id="26ceb-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="26ceb-179">Entry</span></span> | <span data-ttu-id="26ceb-180">Valor</span><span class="sxs-lookup"><span data-stu-id="26ceb-180">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="26ceb-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="26ceb-181">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="26ceb-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26ceb-182">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="26ceb-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="26ceb-183">System-Only</span></span>            | <span data-ttu-id="26ceb-184">Falso</span><span class="sxs-lookup"><span data-stu-id="26ceb-184">False</span></span>                                    |
| <span data-ttu-id="26ceb-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="26ceb-185">Is-Single-Valued</span></span>       | <span data-ttu-id="26ceb-186">True</span><span class="sxs-lookup"><span data-stu-id="26ceb-186">True</span></span>                                     |
| <span data-ttu-id="26ceb-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="26ceb-187">Is Indexed</span></span>             | <span data-ttu-id="26ceb-188">Falso</span><span class="sxs-lookup"><span data-stu-id="26ceb-188">False</span></span>                                    |
| <span data-ttu-id="26ceb-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="26ceb-189">In Global Catalog</span></span>      | <span data-ttu-id="26ceb-190">Falso</span><span class="sxs-lookup"><span data-stu-id="26ceb-190">False</span></span>                                    |
| <span data-ttu-id="26ceb-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="26ceb-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="26ceb-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="26ceb-192">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="26ceb-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26ceb-193">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="26ceb-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26ceb-194">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="26ceb-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26ceb-195">Search-Flags</span></span>           | <span data-ttu-id="26ceb-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26ceb-196">0x00000000</span></span>                               |
| <span data-ttu-id="26ceb-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26ceb-197">System-Flags</span></span>           | <span data-ttu-id="26ceb-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="26ceb-198">0x00000010</span></span>                               |
| <span data-ttu-id="26ceb-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="26ceb-199">Classes used in</span></span>        | [<span data-ttu-id="26ceb-200">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="26ceb-200">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="26ceb-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="26ceb-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="26ceb-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="26ceb-202">Entry</span></span> | <span data-ttu-id="26ceb-203">Valor</span><span class="sxs-lookup"><span data-stu-id="26ceb-203">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="26ceb-204">ID do link</span><span class="sxs-lookup"><span data-stu-id="26ceb-204">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="26ceb-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26ceb-205">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="26ceb-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="26ceb-206">System-Only</span></span>            | <span data-ttu-id="26ceb-207">Falso</span><span class="sxs-lookup"><span data-stu-id="26ceb-207">False</span></span>                                    |
| <span data-ttu-id="26ceb-208">É de valor único</span><span class="sxs-lookup"><span data-stu-id="26ceb-208">Is-Single-Valued</span></span>       | <span data-ttu-id="26ceb-209">True</span><span class="sxs-lookup"><span data-stu-id="26ceb-209">True</span></span>                                     |
| <span data-ttu-id="26ceb-210">É indexado</span><span class="sxs-lookup"><span data-stu-id="26ceb-210">Is Indexed</span></span>             | <span data-ttu-id="26ceb-211">Falso</span><span class="sxs-lookup"><span data-stu-id="26ceb-211">False</span></span>                                    |
| <span data-ttu-id="26ceb-212">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="26ceb-212">In Global Catalog</span></span>      | <span data-ttu-id="26ceb-213">Falso</span><span class="sxs-lookup"><span data-stu-id="26ceb-213">False</span></span>                                    |
| <span data-ttu-id="26ceb-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="26ceb-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="26ceb-215">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="26ceb-215">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="26ceb-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26ceb-216">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="26ceb-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26ceb-217">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="26ceb-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26ceb-218">Search-Flags</span></span>           | <span data-ttu-id="26ceb-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26ceb-219">0x00000000</span></span>                               |
| <span data-ttu-id="26ceb-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26ceb-220">System-Flags</span></span>           | <span data-ttu-id="26ceb-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="26ceb-221">0x00000010</span></span>                               |
| <span data-ttu-id="26ceb-222">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="26ceb-222">Classes used in</span></span>        | [<span data-ttu-id="26ceb-223">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="26ceb-223">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="26ceb-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26ceb-224">Windows Server 2008</span></span>



| <span data-ttu-id="26ceb-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="26ceb-225">Entry</span></span> | <span data-ttu-id="26ceb-226">Valor</span><span class="sxs-lookup"><span data-stu-id="26ceb-226">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="26ceb-227">ID do link</span><span class="sxs-lookup"><span data-stu-id="26ceb-227">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="26ceb-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26ceb-228">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="26ceb-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="26ceb-229">System-Only</span></span>            | <span data-ttu-id="26ceb-230">Falso</span><span class="sxs-lookup"><span data-stu-id="26ceb-230">False</span></span>                                    |
| <span data-ttu-id="26ceb-231">É de valor único</span><span class="sxs-lookup"><span data-stu-id="26ceb-231">Is-Single-Valued</span></span>       | <span data-ttu-id="26ceb-232">True</span><span class="sxs-lookup"><span data-stu-id="26ceb-232">True</span></span>                                     |
| <span data-ttu-id="26ceb-233">É indexado</span><span class="sxs-lookup"><span data-stu-id="26ceb-233">Is Indexed</span></span>             | <span data-ttu-id="26ceb-234">Falso</span><span class="sxs-lookup"><span data-stu-id="26ceb-234">False</span></span>                                    |
| <span data-ttu-id="26ceb-235">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="26ceb-235">In Global Catalog</span></span>      | <span data-ttu-id="26ceb-236">Falso</span><span class="sxs-lookup"><span data-stu-id="26ceb-236">False</span></span>                                    |
| <span data-ttu-id="26ceb-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="26ceb-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="26ceb-238">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="26ceb-238">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="26ceb-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26ceb-239">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="26ceb-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26ceb-240">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="26ceb-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26ceb-241">Search-Flags</span></span>           | <span data-ttu-id="26ceb-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26ceb-242">0x00000000</span></span>                               |
| <span data-ttu-id="26ceb-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26ceb-243">System-Flags</span></span>           | <span data-ttu-id="26ceb-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="26ceb-244">0x00000010</span></span>                               |
| <span data-ttu-id="26ceb-245">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="26ceb-245">Classes used in</span></span>        | [<span data-ttu-id="26ceb-246">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="26ceb-246">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="26ceb-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="26ceb-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="26ceb-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="26ceb-248">Entry</span></span> | <span data-ttu-id="26ceb-249">Valor</span><span class="sxs-lookup"><span data-stu-id="26ceb-249">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="26ceb-250">ID do link</span><span class="sxs-lookup"><span data-stu-id="26ceb-250">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="26ceb-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26ceb-251">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="26ceb-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="26ceb-252">System-Only</span></span>            | <span data-ttu-id="26ceb-253">Falso</span><span class="sxs-lookup"><span data-stu-id="26ceb-253">False</span></span>                                    |
| <span data-ttu-id="26ceb-254">É de valor único</span><span class="sxs-lookup"><span data-stu-id="26ceb-254">Is-Single-Valued</span></span>       | <span data-ttu-id="26ceb-255">True</span><span class="sxs-lookup"><span data-stu-id="26ceb-255">True</span></span>                                     |
| <span data-ttu-id="26ceb-256">É indexado</span><span class="sxs-lookup"><span data-stu-id="26ceb-256">Is Indexed</span></span>             | <span data-ttu-id="26ceb-257">Falso</span><span class="sxs-lookup"><span data-stu-id="26ceb-257">False</span></span>                                    |
| <span data-ttu-id="26ceb-258">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="26ceb-258">In Global Catalog</span></span>      | <span data-ttu-id="26ceb-259">Falso</span><span class="sxs-lookup"><span data-stu-id="26ceb-259">False</span></span>                                    |
| <span data-ttu-id="26ceb-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="26ceb-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="26ceb-261">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="26ceb-261">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="26ceb-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26ceb-262">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="26ceb-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26ceb-263">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="26ceb-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26ceb-264">Search-Flags</span></span>           | <span data-ttu-id="26ceb-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26ceb-265">0x00000000</span></span>                               |
| <span data-ttu-id="26ceb-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26ceb-266">System-Flags</span></span>           | <span data-ttu-id="26ceb-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="26ceb-267">0x00000010</span></span>                               |
| <span data-ttu-id="26ceb-268">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="26ceb-268">Classes used in</span></span>        | [<span data-ttu-id="26ceb-269">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="26ceb-269">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="26ceb-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="26ceb-270">Windows Server 2012</span></span>



| <span data-ttu-id="26ceb-271">Entrada</span><span class="sxs-lookup"><span data-stu-id="26ceb-271">Entry</span></span> | <span data-ttu-id="26ceb-272">Valor</span><span class="sxs-lookup"><span data-stu-id="26ceb-272">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="26ceb-273">ID do link</span><span class="sxs-lookup"><span data-stu-id="26ceb-273">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="26ceb-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="26ceb-274">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="26ceb-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="26ceb-275">System-Only</span></span>            | <span data-ttu-id="26ceb-276">Falso</span><span class="sxs-lookup"><span data-stu-id="26ceb-276">False</span></span>                                    |
| <span data-ttu-id="26ceb-277">É de valor único</span><span class="sxs-lookup"><span data-stu-id="26ceb-277">Is-Single-Valued</span></span>       | <span data-ttu-id="26ceb-278">True</span><span class="sxs-lookup"><span data-stu-id="26ceb-278">True</span></span>                                     |
| <span data-ttu-id="26ceb-279">É indexado</span><span class="sxs-lookup"><span data-stu-id="26ceb-279">Is Indexed</span></span>             | <span data-ttu-id="26ceb-280">Falso</span><span class="sxs-lookup"><span data-stu-id="26ceb-280">False</span></span>                                    |
| <span data-ttu-id="26ceb-281">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="26ceb-281">In Global Catalog</span></span>      | <span data-ttu-id="26ceb-282">Falso</span><span class="sxs-lookup"><span data-stu-id="26ceb-282">False</span></span>                                    |
| <span data-ttu-id="26ceb-283">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="26ceb-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="26ceb-284">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="26ceb-284">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="26ceb-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="26ceb-285">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="26ceb-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="26ceb-286">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="26ceb-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="26ceb-287">Search-Flags</span></span>           | <span data-ttu-id="26ceb-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="26ceb-288">0x00000000</span></span>                               |
| <span data-ttu-id="26ceb-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="26ceb-289">System-Flags</span></span>           | <span data-ttu-id="26ceb-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="26ceb-290">0x00000010</span></span>                               |
| <span data-ttu-id="26ceb-291">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="26ceb-291">Classes used in</span></span>        | [<span data-ttu-id="26ceb-292">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="26ceb-292">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





