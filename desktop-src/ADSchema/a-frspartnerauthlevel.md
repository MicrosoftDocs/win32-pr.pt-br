---
title: FRS-atributo de nível de autenticação de parceiro
description: O nível de segurança RPC.
ms.assetid: ec7a8d92-33c0-415a-bc38-5b7df81226bc
ms.tgt_platform: multiple
keywords:
- FRS-parceiro-do atributo de nível de autenticação esquema do AD
- Esquema de AD do atributo fRSPartnerAuthLevel
topic_type:
- apiref
api_name:
- FRS-Partner-Auth-Level
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10ba4b89c86b654ed434c012a0c2b683bf07c0e7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104369960"
---
# <a name="frs-partner-auth-level-attribute"></a><span data-ttu-id="1b1f8-105">FRS-atributo de nível de autenticação de parceiro</span><span class="sxs-lookup"><span data-stu-id="1b1f8-105">FRS-Partner-Auth-Level attribute</span></span>

<span data-ttu-id="1b1f8-106">O nível de segurança RPC.</span><span class="sxs-lookup"><span data-stu-id="1b1f8-106">The RPC Security level.</span></span>



| <span data-ttu-id="1b1f8-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="1b1f8-107">Entry</span></span> | <span data-ttu-id="1b1f8-108">Valor</span><span class="sxs-lookup"><span data-stu-id="1b1f8-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="1b1f8-109">CN</span><span class="sxs-lookup"><span data-stu-id="1b1f8-109">CN</span></span>                | <span data-ttu-id="1b1f8-110">FRS-parceiro-nível de autenticação</span><span class="sxs-lookup"><span data-stu-id="1b1f8-110">FRS-Partner-Auth-Level</span></span>               |
| <span data-ttu-id="1b1f8-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="1b1f8-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1b1f8-112">fRSPartnerAuthLevel</span><span class="sxs-lookup"><span data-stu-id="1b1f8-112">fRSPartnerAuthLevel</span></span>                  |
| <span data-ttu-id="1b1f8-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="1b1f8-113">Size</span></span>              | <span data-ttu-id="1b1f8-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="1b1f8-114">4 bytes</span></span>                              |
| <span data-ttu-id="1b1f8-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="1b1f8-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="1b1f8-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="1b1f8-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="1b1f8-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1b1f8-117">Attribute-Id</span></span>      | <span data-ttu-id="1b1f8-118">1.2.840.113556.1.4.877</span><span class="sxs-lookup"><span data-stu-id="1b1f8-118">1.2.840.113556.1.4.877</span></span>               |
| <span data-ttu-id="1b1f8-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1b1f8-119">System-Id-Guid</span></span>    | <span data-ttu-id="1b1f8-120">2a132580-9373-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="1b1f8-120">2a132580-9373-11d1-aebc-0000f80367c1</span></span> |
| <span data-ttu-id="1b1f8-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b1f8-121">Syntax</span></span>            | [<span data-ttu-id="1b1f8-122">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="1b1f8-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="1b1f8-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="1b1f8-123">Implementations</span></span>

-   [<span data-ttu-id="1b1f8-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1b1f8-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1b1f8-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1b1f8-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1b1f8-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1b1f8-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1b1f8-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1b1f8-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1b1f8-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1b1f8-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1b1f8-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1b1f8-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1b1f8-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1b1f8-130">Windows 2000 Server</span></span>



| <span data-ttu-id="1b1f8-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="1b1f8-131">Entry</span></span> | <span data-ttu-id="1b1f8-132">Valor</span><span class="sxs-lookup"><span data-stu-id="1b1f8-132">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b1f8-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="1b1f8-133">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1b1f8-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b1f8-134">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1b1f8-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b1f8-135">System-Only</span></span>            | <span data-ttu-id="1b1f8-136">Falso</span><span class="sxs-lookup"><span data-stu-id="1b1f8-136">False</span></span>                                                                                                      |
| <span data-ttu-id="1b1f8-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1b1f8-137">Is-Single-Valued</span></span>       | <span data-ttu-id="1b1f8-138">True</span><span class="sxs-lookup"><span data-stu-id="1b1f8-138">True</span></span>                                                                                                       |
| <span data-ttu-id="1b1f8-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="1b1f8-139">Is Indexed</span></span>             | <span data-ttu-id="1b1f8-140">Falso</span><span class="sxs-lookup"><span data-stu-id="1b1f8-140">False</span></span>                                                                                                      |
| <span data-ttu-id="1b1f8-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1b1f8-141">In Global Catalog</span></span>      | <span data-ttu-id="1b1f8-142">Falso</span><span class="sxs-lookup"><span data-stu-id="1b1f8-142">False</span></span>                                                                                                      |
| <span data-ttu-id="1b1f8-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1b1f8-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b1f8-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1b1f8-144">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="1b1f8-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b1f8-145">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="1b1f8-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b1f8-146">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="1b1f8-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b1f8-147">Search-Flags</span></span>           | <span data-ttu-id="1b1f8-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b1f8-148">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="1b1f8-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b1f8-149">System-Flags</span></span>           | <span data-ttu-id="1b1f8-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b1f8-150">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="1b1f8-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1b1f8-151">Classes used in</span></span>        | [<span data-ttu-id="1b1f8-152">**NTFRS-membro**</span><span class="sxs-lookup"><span data-stu-id="1b1f8-152">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="1b1f8-153">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="1b1f8-153">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1b1f8-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1b1f8-154">Windows Server 2003</span></span>



| <span data-ttu-id="1b1f8-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="1b1f8-155">Entry</span></span> | <span data-ttu-id="1b1f8-156">Valor</span><span class="sxs-lookup"><span data-stu-id="1b1f8-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b1f8-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="1b1f8-157">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1b1f8-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b1f8-158">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1b1f8-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b1f8-159">System-Only</span></span>            | <span data-ttu-id="1b1f8-160">Falso</span><span class="sxs-lookup"><span data-stu-id="1b1f8-160">False</span></span>                                                                                                      |
| <span data-ttu-id="1b1f8-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1b1f8-161">Is-Single-Valued</span></span>       | <span data-ttu-id="1b1f8-162">True</span><span class="sxs-lookup"><span data-stu-id="1b1f8-162">True</span></span>                                                                                                       |
| <span data-ttu-id="1b1f8-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="1b1f8-163">Is Indexed</span></span>             | <span data-ttu-id="1b1f8-164">Falso</span><span class="sxs-lookup"><span data-stu-id="1b1f8-164">False</span></span>                                                                                                      |
| <span data-ttu-id="1b1f8-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1b1f8-165">In Global Catalog</span></span>      | <span data-ttu-id="1b1f8-166">Falso</span><span class="sxs-lookup"><span data-stu-id="1b1f8-166">False</span></span>                                                                                                      |
| <span data-ttu-id="1b1f8-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1b1f8-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b1f8-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1b1f8-168">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="1b1f8-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b1f8-169">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="1b1f8-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b1f8-170">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="1b1f8-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b1f8-171">Search-Flags</span></span>           | <span data-ttu-id="1b1f8-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b1f8-172">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="1b1f8-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b1f8-173">System-Flags</span></span>           | <span data-ttu-id="1b1f8-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b1f8-174">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="1b1f8-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1b1f8-175">Classes used in</span></span>        | [<span data-ttu-id="1b1f8-176">**NTFRS-membro**</span><span class="sxs-lookup"><span data-stu-id="1b1f8-176">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="1b1f8-177">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="1b1f8-177">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1b1f8-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1b1f8-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1b1f8-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="1b1f8-179">Entry</span></span> | <span data-ttu-id="1b1f8-180">Valor</span><span class="sxs-lookup"><span data-stu-id="1b1f8-180">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b1f8-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="1b1f8-181">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1b1f8-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b1f8-182">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1b1f8-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b1f8-183">System-Only</span></span>            | <span data-ttu-id="1b1f8-184">Falso</span><span class="sxs-lookup"><span data-stu-id="1b1f8-184">False</span></span>                                                                                                      |
| <span data-ttu-id="1b1f8-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1b1f8-185">Is-Single-Valued</span></span>       | <span data-ttu-id="1b1f8-186">True</span><span class="sxs-lookup"><span data-stu-id="1b1f8-186">True</span></span>                                                                                                       |
| <span data-ttu-id="1b1f8-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="1b1f8-187">Is Indexed</span></span>             | <span data-ttu-id="1b1f8-188">Falso</span><span class="sxs-lookup"><span data-stu-id="1b1f8-188">False</span></span>                                                                                                      |
| <span data-ttu-id="1b1f8-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1b1f8-189">In Global Catalog</span></span>      | <span data-ttu-id="1b1f8-190">Falso</span><span class="sxs-lookup"><span data-stu-id="1b1f8-190">False</span></span>                                                                                                      |
| <span data-ttu-id="1b1f8-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1b1f8-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b1f8-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1b1f8-192">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="1b1f8-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b1f8-193">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="1b1f8-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b1f8-194">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="1b1f8-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b1f8-195">Search-Flags</span></span>           | <span data-ttu-id="1b1f8-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b1f8-196">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="1b1f8-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b1f8-197">System-Flags</span></span>           | <span data-ttu-id="1b1f8-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b1f8-198">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="1b1f8-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1b1f8-199">Classes used in</span></span>        | [<span data-ttu-id="1b1f8-200">**NTFRS-membro**</span><span class="sxs-lookup"><span data-stu-id="1b1f8-200">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="1b1f8-201">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="1b1f8-201">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1b1f8-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1b1f8-202">Windows Server 2008</span></span>



| <span data-ttu-id="1b1f8-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="1b1f8-203">Entry</span></span> | <span data-ttu-id="1b1f8-204">Valor</span><span class="sxs-lookup"><span data-stu-id="1b1f8-204">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b1f8-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="1b1f8-205">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1b1f8-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b1f8-206">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1b1f8-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b1f8-207">System-Only</span></span>            | <span data-ttu-id="1b1f8-208">Falso</span><span class="sxs-lookup"><span data-stu-id="1b1f8-208">False</span></span>                                                                                                      |
| <span data-ttu-id="1b1f8-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1b1f8-209">Is-Single-Valued</span></span>       | <span data-ttu-id="1b1f8-210">True</span><span class="sxs-lookup"><span data-stu-id="1b1f8-210">True</span></span>                                                                                                       |
| <span data-ttu-id="1b1f8-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="1b1f8-211">Is Indexed</span></span>             | <span data-ttu-id="1b1f8-212">Falso</span><span class="sxs-lookup"><span data-stu-id="1b1f8-212">False</span></span>                                                                                                      |
| <span data-ttu-id="1b1f8-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1b1f8-213">In Global Catalog</span></span>      | <span data-ttu-id="1b1f8-214">Falso</span><span class="sxs-lookup"><span data-stu-id="1b1f8-214">False</span></span>                                                                                                      |
| <span data-ttu-id="1b1f8-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1b1f8-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b1f8-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1b1f8-216">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="1b1f8-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b1f8-217">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="1b1f8-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b1f8-218">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="1b1f8-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b1f8-219">Search-Flags</span></span>           | <span data-ttu-id="1b1f8-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b1f8-220">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="1b1f8-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b1f8-221">System-Flags</span></span>           | <span data-ttu-id="1b1f8-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b1f8-222">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="1b1f8-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1b1f8-223">Classes used in</span></span>        | [<span data-ttu-id="1b1f8-224">**NTFRS-membro**</span><span class="sxs-lookup"><span data-stu-id="1b1f8-224">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="1b1f8-225">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="1b1f8-225">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1b1f8-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1b1f8-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1b1f8-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="1b1f8-227">Entry</span></span> | <span data-ttu-id="1b1f8-228">Valor</span><span class="sxs-lookup"><span data-stu-id="1b1f8-228">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b1f8-229">ID do link</span><span class="sxs-lookup"><span data-stu-id="1b1f8-229">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1b1f8-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b1f8-230">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1b1f8-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b1f8-231">System-Only</span></span>            | <span data-ttu-id="1b1f8-232">Falso</span><span class="sxs-lookup"><span data-stu-id="1b1f8-232">False</span></span>                                                                                                      |
| <span data-ttu-id="1b1f8-233">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1b1f8-233">Is-Single-Valued</span></span>       | <span data-ttu-id="1b1f8-234">True</span><span class="sxs-lookup"><span data-stu-id="1b1f8-234">True</span></span>                                                                                                       |
| <span data-ttu-id="1b1f8-235">É indexado</span><span class="sxs-lookup"><span data-stu-id="1b1f8-235">Is Indexed</span></span>             | <span data-ttu-id="1b1f8-236">Falso</span><span class="sxs-lookup"><span data-stu-id="1b1f8-236">False</span></span>                                                                                                      |
| <span data-ttu-id="1b1f8-237">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1b1f8-237">In Global Catalog</span></span>      | <span data-ttu-id="1b1f8-238">Falso</span><span class="sxs-lookup"><span data-stu-id="1b1f8-238">False</span></span>                                                                                                      |
| <span data-ttu-id="1b1f8-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1b1f8-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b1f8-240">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1b1f8-240">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="1b1f8-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b1f8-241">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="1b1f8-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b1f8-242">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="1b1f8-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b1f8-243">Search-Flags</span></span>           | <span data-ttu-id="1b1f8-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b1f8-244">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="1b1f8-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b1f8-245">System-Flags</span></span>           | <span data-ttu-id="1b1f8-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b1f8-246">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="1b1f8-247">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1b1f8-247">Classes used in</span></span>        | [<span data-ttu-id="1b1f8-248">**NTFRS-membro**</span><span class="sxs-lookup"><span data-stu-id="1b1f8-248">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="1b1f8-249">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="1b1f8-249">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1b1f8-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1b1f8-250">Windows Server 2012</span></span>



| <span data-ttu-id="1b1f8-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="1b1f8-251">Entry</span></span> | <span data-ttu-id="1b1f8-252">Valor</span><span class="sxs-lookup"><span data-stu-id="1b1f8-252">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b1f8-253">ID do link</span><span class="sxs-lookup"><span data-stu-id="1b1f8-253">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1b1f8-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1b1f8-254">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="1b1f8-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="1b1f8-255">System-Only</span></span>            | <span data-ttu-id="1b1f8-256">Falso</span><span class="sxs-lookup"><span data-stu-id="1b1f8-256">False</span></span>                                                                                                      |
| <span data-ttu-id="1b1f8-257">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1b1f8-257">Is-Single-Valued</span></span>       | <span data-ttu-id="1b1f8-258">True</span><span class="sxs-lookup"><span data-stu-id="1b1f8-258">True</span></span>                                                                                                       |
| <span data-ttu-id="1b1f8-259">É indexado</span><span class="sxs-lookup"><span data-stu-id="1b1f8-259">Is Indexed</span></span>             | <span data-ttu-id="1b1f8-260">Falso</span><span class="sxs-lookup"><span data-stu-id="1b1f8-260">False</span></span>                                                                                                      |
| <span data-ttu-id="1b1f8-261">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1b1f8-261">In Global Catalog</span></span>      | <span data-ttu-id="1b1f8-262">Falso</span><span class="sxs-lookup"><span data-stu-id="1b1f8-262">False</span></span>                                                                                                      |
| <span data-ttu-id="1b1f8-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1b1f8-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="1b1f8-264">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1b1f8-264">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="1b1f8-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1b1f8-265">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="1b1f8-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1b1f8-266">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="1b1f8-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1b1f8-267">Search-Flags</span></span>           | <span data-ttu-id="1b1f8-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b1f8-268">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="1b1f8-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1b1f8-269">System-Flags</span></span>           | <span data-ttu-id="1b1f8-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1b1f8-270">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="1b1f8-271">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1b1f8-271">Classes used in</span></span>        | [<span data-ttu-id="1b1f8-272">**NTFRS-membro**</span><span class="sxs-lookup"><span data-stu-id="1b1f8-272">**NTFRS-Member**</span></span>](c-ntfrsmember.md)<br/> [<span data-ttu-id="1b1f8-273">**NTFRS-conjunto de réplicas**</span><span class="sxs-lookup"><span data-stu-id="1b1f8-273">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





