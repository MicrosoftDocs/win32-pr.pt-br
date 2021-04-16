---
title: atributo ms-DS-logon-time-Sync-Interval
description: Esse atributo controla a granularidade, em dias, com a qual a hora do último logon de um usuário ou computador, registrada no atributo lastLogonTimestamp, é replicada para todos os DCs em um domínio.
ms.assetid: f1f9f1f8-df60-44b5-965d-631c4dd4ef84
ms.tgt_platform: multiple
keywords:
- ms-DS-login-time-Synchronization-Interval atributo AD Schema
- atributo msDS-LogonTimeSyncInterval do AD Schema
topic_type:
- apiref
api_name:
- ms-DS-Logon-Time-Sync-Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dbf23ca77bda9dac76f02986be1c05c80559199
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104500078"
---
# <a name="ms-ds-logon-time-sync-interval-attribute"></a><span data-ttu-id="c1dd9-105">atributo ms-DS-logon-time-Sync-Interval</span><span class="sxs-lookup"><span data-stu-id="c1dd9-105">ms-DS-Logon-Time-Sync-Interval attribute</span></span>

<span data-ttu-id="c1dd9-106">Esse atributo controla a granularidade, em dias, com a qual a hora do último logon de um usuário ou computador, registrada no atributo lastLogonTimestamp, é replicada para todos os DCs em um domínio.</span><span class="sxs-lookup"><span data-stu-id="c1dd9-106">This attribute controls the granularity, in days, with which the last logon time for a user or computer, recorded in the lastLogonTimestamp attribute, is replicated to all DCs in a domain.</span></span>



| <span data-ttu-id="c1dd9-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="c1dd9-107">Entry</span></span> | <span data-ttu-id="c1dd9-108">Valor</span><span class="sxs-lookup"><span data-stu-id="c1dd9-108">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1dd9-109">CN</span><span class="sxs-lookup"><span data-stu-id="c1dd9-109">CN</span></span>                | <span data-ttu-id="c1dd9-110">ms-DS-logon-time-Sync-Interval</span><span class="sxs-lookup"><span data-stu-id="c1dd9-110">ms-DS-Logon-Time-Sync-Interval</span></span>                                                                             |
| <span data-ttu-id="c1dd9-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c1dd9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c1dd9-112">msDS-LogonTimeSyncInterval</span><span class="sxs-lookup"><span data-stu-id="c1dd9-112">msDS-LogonTimeSyncInterval</span></span>                                                                                 |
| <span data-ttu-id="c1dd9-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="c1dd9-113">Size</span></span>              | <span data-ttu-id="c1dd9-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="c1dd9-114">4 bytes</span></span>                                                                                                    |
| <span data-ttu-id="c1dd9-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="c1dd9-115">Update Privilege</span></span>  | <span data-ttu-id="c1dd9-116">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="c1dd9-116">Domain administrator</span></span>                                                                                       |
| <span data-ttu-id="c1dd9-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="c1dd9-117">Update Frequency</span></span>  | <span data-ttu-id="c1dd9-118">Raramente, como essa é uma configuração de política, ela é atualizada somente quando uma alteração na política de todo o domínio é desejada.</span><span class="sxs-lookup"><span data-stu-id="c1dd9-118">Rarely, since this is a policy setting, it is updated only when a change in domain-wide policy is desired.</span></span> |
| <span data-ttu-id="c1dd9-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c1dd9-119">Attribute-Id</span></span>      | <span data-ttu-id="c1dd9-120">1.2.840.113556.1.4.1784</span><span class="sxs-lookup"><span data-stu-id="c1dd9-120">1.2.840.113556.1.4.1784</span></span>                                                                                    |
| <span data-ttu-id="c1dd9-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c1dd9-121">System-Id-Guid</span></span>    | <span data-ttu-id="c1dd9-122">ad7940f8-e43a-4a42-83bc-d688e59ea605</span><span class="sxs-lookup"><span data-stu-id="c1dd9-122">ad7940f8-e43a-4a42-83bc-d688e59ea605</span></span>                                                                       |
| <span data-ttu-id="c1dd9-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1dd9-123">Syntax</span></span>            | [<span data-ttu-id="c1dd9-124">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="c1dd9-124">**Enumeration**</span></span>](s-enumeration.md)                                                                       |



## <a name="implementations"></a><span data-ttu-id="c1dd9-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="c1dd9-125">Implementations</span></span>

-   [<span data-ttu-id="c1dd9-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c1dd9-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c1dd9-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c1dd9-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c1dd9-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c1dd9-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c1dd9-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c1dd9-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c1dd9-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c1dd9-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="c1dd9-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c1dd9-131">Windows Server 2003</span></span>



| <span data-ttu-id="c1dd9-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="c1dd9-132">Entry</span></span> | <span data-ttu-id="c1dd9-133">Valor</span><span class="sxs-lookup"><span data-stu-id="c1dd9-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c1dd9-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="c1dd9-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c1dd9-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1dd9-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c1dd9-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1dd9-136">System-Only</span></span>            | <span data-ttu-id="c1dd9-137">Falso</span><span class="sxs-lookup"><span data-stu-id="c1dd9-137">False</span></span>                                        |
| <span data-ttu-id="c1dd9-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c1dd9-138">Is-Single-Valued</span></span>       | <span data-ttu-id="c1dd9-139">True</span><span class="sxs-lookup"><span data-stu-id="c1dd9-139">True</span></span>                                         |
| <span data-ttu-id="c1dd9-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="c1dd9-140">Is Indexed</span></span>             | <span data-ttu-id="c1dd9-141">Falso</span><span class="sxs-lookup"><span data-stu-id="c1dd9-141">False</span></span>                                        |
| <span data-ttu-id="c1dd9-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c1dd9-142">In Global Catalog</span></span>      | <span data-ttu-id="c1dd9-143">Falso</span><span class="sxs-lookup"><span data-stu-id="c1dd9-143">False</span></span>                                        |
| <span data-ttu-id="c1dd9-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c1dd9-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1dd9-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c1dd9-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c1dd9-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1dd9-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c1dd9-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1dd9-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c1dd9-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1dd9-148">Search-Flags</span></span>           | <span data-ttu-id="c1dd9-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1dd9-149">0x00000000</span></span>                                   |
| <span data-ttu-id="c1dd9-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1dd9-150">System-Flags</span></span>           | <span data-ttu-id="c1dd9-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1dd9-151">0x00000010</span></span>                                   |
| <span data-ttu-id="c1dd9-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c1dd9-152">Classes used in</span></span>        | [<span data-ttu-id="c1dd9-153">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="c1dd9-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c1dd9-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c1dd9-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c1dd9-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="c1dd9-155">Entry</span></span> | <span data-ttu-id="c1dd9-156">Valor</span><span class="sxs-lookup"><span data-stu-id="c1dd9-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c1dd9-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="c1dd9-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c1dd9-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1dd9-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c1dd9-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1dd9-159">System-Only</span></span>            | <span data-ttu-id="c1dd9-160">Falso</span><span class="sxs-lookup"><span data-stu-id="c1dd9-160">False</span></span>                                        |
| <span data-ttu-id="c1dd9-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c1dd9-161">Is-Single-Valued</span></span>       | <span data-ttu-id="c1dd9-162">True</span><span class="sxs-lookup"><span data-stu-id="c1dd9-162">True</span></span>                                         |
| <span data-ttu-id="c1dd9-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="c1dd9-163">Is Indexed</span></span>             | <span data-ttu-id="c1dd9-164">Falso</span><span class="sxs-lookup"><span data-stu-id="c1dd9-164">False</span></span>                                        |
| <span data-ttu-id="c1dd9-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c1dd9-165">In Global Catalog</span></span>      | <span data-ttu-id="c1dd9-166">Falso</span><span class="sxs-lookup"><span data-stu-id="c1dd9-166">False</span></span>                                        |
| <span data-ttu-id="c1dd9-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c1dd9-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1dd9-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c1dd9-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c1dd9-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1dd9-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c1dd9-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1dd9-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c1dd9-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1dd9-171">Search-Flags</span></span>           | <span data-ttu-id="c1dd9-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1dd9-172">0x00000000</span></span>                                   |
| <span data-ttu-id="c1dd9-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1dd9-173">System-Flags</span></span>           | <span data-ttu-id="c1dd9-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1dd9-174">0x00000010</span></span>                                   |
| <span data-ttu-id="c1dd9-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c1dd9-175">Classes used in</span></span>        | [<span data-ttu-id="c1dd9-176">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="c1dd9-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c1dd9-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c1dd9-177">Windows Server 2008</span></span>



| <span data-ttu-id="c1dd9-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="c1dd9-178">Entry</span></span> | <span data-ttu-id="c1dd9-179">Valor</span><span class="sxs-lookup"><span data-stu-id="c1dd9-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c1dd9-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="c1dd9-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c1dd9-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1dd9-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c1dd9-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1dd9-182">System-Only</span></span>            | <span data-ttu-id="c1dd9-183">Falso</span><span class="sxs-lookup"><span data-stu-id="c1dd9-183">False</span></span>                                        |
| <span data-ttu-id="c1dd9-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c1dd9-184">Is-Single-Valued</span></span>       | <span data-ttu-id="c1dd9-185">True</span><span class="sxs-lookup"><span data-stu-id="c1dd9-185">True</span></span>                                         |
| <span data-ttu-id="c1dd9-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="c1dd9-186">Is Indexed</span></span>             | <span data-ttu-id="c1dd9-187">Falso</span><span class="sxs-lookup"><span data-stu-id="c1dd9-187">False</span></span>                                        |
| <span data-ttu-id="c1dd9-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c1dd9-188">In Global Catalog</span></span>      | <span data-ttu-id="c1dd9-189">Falso</span><span class="sxs-lookup"><span data-stu-id="c1dd9-189">False</span></span>                                        |
| <span data-ttu-id="c1dd9-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c1dd9-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1dd9-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c1dd9-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c1dd9-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1dd9-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c1dd9-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1dd9-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c1dd9-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1dd9-194">Search-Flags</span></span>           | <span data-ttu-id="c1dd9-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1dd9-195">0x00000000</span></span>                                   |
| <span data-ttu-id="c1dd9-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1dd9-196">System-Flags</span></span>           | <span data-ttu-id="c1dd9-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1dd9-197">0x00000010</span></span>                                   |
| <span data-ttu-id="c1dd9-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c1dd9-198">Classes used in</span></span>        | [<span data-ttu-id="c1dd9-199">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="c1dd9-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c1dd9-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c1dd9-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c1dd9-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="c1dd9-201">Entry</span></span> | <span data-ttu-id="c1dd9-202">Valor</span><span class="sxs-lookup"><span data-stu-id="c1dd9-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c1dd9-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="c1dd9-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c1dd9-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1dd9-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c1dd9-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1dd9-205">System-Only</span></span>            | <span data-ttu-id="c1dd9-206">Falso</span><span class="sxs-lookup"><span data-stu-id="c1dd9-206">False</span></span>                                        |
| <span data-ttu-id="c1dd9-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c1dd9-207">Is-Single-Valued</span></span>       | <span data-ttu-id="c1dd9-208">True</span><span class="sxs-lookup"><span data-stu-id="c1dd9-208">True</span></span>                                         |
| <span data-ttu-id="c1dd9-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="c1dd9-209">Is Indexed</span></span>             | <span data-ttu-id="c1dd9-210">Falso</span><span class="sxs-lookup"><span data-stu-id="c1dd9-210">False</span></span>                                        |
| <span data-ttu-id="c1dd9-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c1dd9-211">In Global Catalog</span></span>      | <span data-ttu-id="c1dd9-212">Falso</span><span class="sxs-lookup"><span data-stu-id="c1dd9-212">False</span></span>                                        |
| <span data-ttu-id="c1dd9-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c1dd9-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1dd9-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c1dd9-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c1dd9-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1dd9-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c1dd9-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1dd9-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c1dd9-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1dd9-217">Search-Flags</span></span>           | <span data-ttu-id="c1dd9-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1dd9-218">0x00000000</span></span>                                   |
| <span data-ttu-id="c1dd9-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1dd9-219">System-Flags</span></span>           | <span data-ttu-id="c1dd9-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1dd9-220">0x00000010</span></span>                                   |
| <span data-ttu-id="c1dd9-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c1dd9-221">Classes used in</span></span>        | [<span data-ttu-id="c1dd9-222">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="c1dd9-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c1dd9-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c1dd9-223">Windows Server 2012</span></span>



| <span data-ttu-id="c1dd9-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="c1dd9-224">Entry</span></span> | <span data-ttu-id="c1dd9-225">Valor</span><span class="sxs-lookup"><span data-stu-id="c1dd9-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c1dd9-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="c1dd9-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c1dd9-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1dd9-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c1dd9-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1dd9-228">System-Only</span></span>            | <span data-ttu-id="c1dd9-229">Falso</span><span class="sxs-lookup"><span data-stu-id="c1dd9-229">False</span></span>                                        |
| <span data-ttu-id="c1dd9-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c1dd9-230">Is-Single-Valued</span></span>       | <span data-ttu-id="c1dd9-231">True</span><span class="sxs-lookup"><span data-stu-id="c1dd9-231">True</span></span>                                         |
| <span data-ttu-id="c1dd9-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="c1dd9-232">Is Indexed</span></span>             | <span data-ttu-id="c1dd9-233">Falso</span><span class="sxs-lookup"><span data-stu-id="c1dd9-233">False</span></span>                                        |
| <span data-ttu-id="c1dd9-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c1dd9-234">In Global Catalog</span></span>      | <span data-ttu-id="c1dd9-235">Falso</span><span class="sxs-lookup"><span data-stu-id="c1dd9-235">False</span></span>                                        |
| <span data-ttu-id="c1dd9-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c1dd9-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1dd9-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c1dd9-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c1dd9-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1dd9-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c1dd9-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1dd9-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c1dd9-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1dd9-240">Search-Flags</span></span>           | <span data-ttu-id="c1dd9-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1dd9-241">0x00000000</span></span>                                   |
| <span data-ttu-id="c1dd9-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1dd9-242">System-Flags</span></span>           | <span data-ttu-id="c1dd9-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1dd9-243">0x00000010</span></span>                                   |
| <span data-ttu-id="c1dd9-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c1dd9-244">Classes used in</span></span>        | [<span data-ttu-id="c1dd9-245">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="c1dd9-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





