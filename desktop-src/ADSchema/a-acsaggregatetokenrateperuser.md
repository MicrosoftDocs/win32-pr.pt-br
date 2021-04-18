---
title: ACS-Aggregate-token-taxa por atributo de usuário
description: A taxa máxima de token que qualquer usuário pode ter para todos os fluxos.
ms.assetid: a617dce4-bade-40bb-ad99-6025e85bfac5
ms.tgt_platform: multiple
keywords:
- ACS-Aggregate-token-taxa por esquema do AD de atributos por usuário
- Esquema de AD do atributo aCSAggregateTokenRatePerUser
topic_type:
- apiref
api_name:
- ACS-Aggregate-Token-Rate-Per-User
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db1a614e4e2a547d7922bcf47d026337b5e1ba94
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105755696"
---
# <a name="acs-aggregate-token-rate-per-user-attribute"></a><span data-ttu-id="f7efd-105">ACS-Aggregate-token-taxa por atributo de usuário</span><span class="sxs-lookup"><span data-stu-id="f7efd-105">ACS-Aggregate-Token-Rate-Per-User attribute</span></span>

<span data-ttu-id="f7efd-106">A taxa máxima de token que qualquer usuário pode ter para todos os fluxos.</span><span class="sxs-lookup"><span data-stu-id="f7efd-106">The maximum token rate any user may have for all flows.</span></span>



| <span data-ttu-id="f7efd-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7efd-107">Entry</span></span> | <span data-ttu-id="f7efd-108">Valor</span><span class="sxs-lookup"><span data-stu-id="f7efd-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="f7efd-109">CN</span><span class="sxs-lookup"><span data-stu-id="f7efd-109">CN</span></span>                | <span data-ttu-id="f7efd-110">ACS-Aggregate-token-taxa por usuário</span><span class="sxs-lookup"><span data-stu-id="f7efd-110">ACS-Aggregate-Token-Rate-Per-User</span></span>    |
| <span data-ttu-id="f7efd-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f7efd-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f7efd-112">aCSAggregateTokenRatePerUser</span><span class="sxs-lookup"><span data-stu-id="f7efd-112">aCSAggregateTokenRatePerUser</span></span>         |
| <span data-ttu-id="f7efd-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="f7efd-113">Size</span></span>              | <span data-ttu-id="f7efd-114">8 bytes</span><span class="sxs-lookup"><span data-stu-id="f7efd-114">8 bytes</span></span>                              |
| <span data-ttu-id="f7efd-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="f7efd-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="f7efd-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="f7efd-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="f7efd-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f7efd-117">Attribute-Id</span></span>      | <span data-ttu-id="f7efd-118">1.2.840.113556.1.4.760</span><span class="sxs-lookup"><span data-stu-id="f7efd-118">1.2.840.113556.1.4.760</span></span>               |
| <span data-ttu-id="f7efd-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f7efd-119">System-Id-Guid</span></span>    | <span data-ttu-id="f7efd-120">7f56127d-5301-11d1-a9c5-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="f7efd-120">7f56127d-5301-11d1-a9c5-0000f80367c1</span></span> |
| <span data-ttu-id="f7efd-121">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f7efd-121">Syntax</span></span>            | [<span data-ttu-id="f7efd-122">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="f7efd-122">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="f7efd-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="f7efd-123">Implementations</span></span>

-   [<span data-ttu-id="f7efd-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f7efd-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f7efd-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f7efd-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f7efd-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f7efd-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f7efd-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f7efd-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f7efd-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f7efd-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f7efd-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f7efd-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f7efd-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f7efd-130">Windows 2000 Server</span></span>



| <span data-ttu-id="f7efd-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7efd-131">Entry</span></span> | <span data-ttu-id="f7efd-132">Valor</span><span class="sxs-lookup"><span data-stu-id="f7efd-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="f7efd-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="f7efd-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="f7efd-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7efd-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="f7efd-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7efd-135">System-Only</span></span>            | <span data-ttu-id="f7efd-136">Falso</span><span class="sxs-lookup"><span data-stu-id="f7efd-136">False</span></span>                                        |
| <span data-ttu-id="f7efd-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f7efd-137">Is-Single-Valued</span></span>       | <span data-ttu-id="f7efd-138">True</span><span class="sxs-lookup"><span data-stu-id="f7efd-138">True</span></span>                                         |
| <span data-ttu-id="f7efd-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="f7efd-139">Is Indexed</span></span>             | <span data-ttu-id="f7efd-140">Falso</span><span class="sxs-lookup"><span data-stu-id="f7efd-140">False</span></span>                                        |
| <span data-ttu-id="f7efd-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f7efd-141">In Global Catalog</span></span>      | <span data-ttu-id="f7efd-142">Falso</span><span class="sxs-lookup"><span data-stu-id="f7efd-142">False</span></span>                                        |
| <span data-ttu-id="f7efd-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f7efd-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7efd-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f7efd-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="f7efd-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7efd-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="f7efd-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7efd-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="f7efd-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7efd-147">Search-Flags</span></span>           | <span data-ttu-id="f7efd-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7efd-148">0x00000000</span></span>                                   |
| <span data-ttu-id="f7efd-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7efd-149">System-Flags</span></span>           | <span data-ttu-id="f7efd-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7efd-150">0x00000010</span></span>                                   |
| <span data-ttu-id="f7efd-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f7efd-151">Classes used in</span></span>        | [<span data-ttu-id="f7efd-152">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="f7efd-152">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f7efd-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f7efd-153">Windows Server 2003</span></span>



| <span data-ttu-id="f7efd-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7efd-154">Entry</span></span> | <span data-ttu-id="f7efd-155">Valor</span><span class="sxs-lookup"><span data-stu-id="f7efd-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="f7efd-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="f7efd-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="f7efd-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7efd-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="f7efd-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7efd-158">System-Only</span></span>            | <span data-ttu-id="f7efd-159">Falso</span><span class="sxs-lookup"><span data-stu-id="f7efd-159">False</span></span>                                        |
| <span data-ttu-id="f7efd-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f7efd-160">Is-Single-Valued</span></span>       | <span data-ttu-id="f7efd-161">True</span><span class="sxs-lookup"><span data-stu-id="f7efd-161">True</span></span>                                         |
| <span data-ttu-id="f7efd-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="f7efd-162">Is Indexed</span></span>             | <span data-ttu-id="f7efd-163">Falso</span><span class="sxs-lookup"><span data-stu-id="f7efd-163">False</span></span>                                        |
| <span data-ttu-id="f7efd-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f7efd-164">In Global Catalog</span></span>      | <span data-ttu-id="f7efd-165">Falso</span><span class="sxs-lookup"><span data-stu-id="f7efd-165">False</span></span>                                        |
| <span data-ttu-id="f7efd-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f7efd-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7efd-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f7efd-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="f7efd-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7efd-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="f7efd-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7efd-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="f7efd-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7efd-170">Search-Flags</span></span>           | <span data-ttu-id="f7efd-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7efd-171">0x00000000</span></span>                                   |
| <span data-ttu-id="f7efd-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7efd-172">System-Flags</span></span>           | <span data-ttu-id="f7efd-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7efd-173">0x00000010</span></span>                                   |
| <span data-ttu-id="f7efd-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f7efd-174">Classes used in</span></span>        | [<span data-ttu-id="f7efd-175">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="f7efd-175">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f7efd-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f7efd-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f7efd-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7efd-177">Entry</span></span> | <span data-ttu-id="f7efd-178">Valor</span><span class="sxs-lookup"><span data-stu-id="f7efd-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="f7efd-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="f7efd-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="f7efd-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7efd-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="f7efd-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7efd-181">System-Only</span></span>            | <span data-ttu-id="f7efd-182">Falso</span><span class="sxs-lookup"><span data-stu-id="f7efd-182">False</span></span>                                        |
| <span data-ttu-id="f7efd-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f7efd-183">Is-Single-Valued</span></span>       | <span data-ttu-id="f7efd-184">True</span><span class="sxs-lookup"><span data-stu-id="f7efd-184">True</span></span>                                         |
| <span data-ttu-id="f7efd-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="f7efd-185">Is Indexed</span></span>             | <span data-ttu-id="f7efd-186">Falso</span><span class="sxs-lookup"><span data-stu-id="f7efd-186">False</span></span>                                        |
| <span data-ttu-id="f7efd-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f7efd-187">In Global Catalog</span></span>      | <span data-ttu-id="f7efd-188">Falso</span><span class="sxs-lookup"><span data-stu-id="f7efd-188">False</span></span>                                        |
| <span data-ttu-id="f7efd-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f7efd-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7efd-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f7efd-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="f7efd-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7efd-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="f7efd-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7efd-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="f7efd-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7efd-193">Search-Flags</span></span>           | <span data-ttu-id="f7efd-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7efd-194">0x00000000</span></span>                                   |
| <span data-ttu-id="f7efd-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7efd-195">System-Flags</span></span>           | <span data-ttu-id="f7efd-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7efd-196">0x00000010</span></span>                                   |
| <span data-ttu-id="f7efd-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f7efd-197">Classes used in</span></span>        | [<span data-ttu-id="f7efd-198">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="f7efd-198">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f7efd-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7efd-199">Windows Server 2008</span></span>



| <span data-ttu-id="f7efd-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7efd-200">Entry</span></span> | <span data-ttu-id="f7efd-201">Valor</span><span class="sxs-lookup"><span data-stu-id="f7efd-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="f7efd-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="f7efd-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="f7efd-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7efd-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="f7efd-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7efd-204">System-Only</span></span>            | <span data-ttu-id="f7efd-205">Falso</span><span class="sxs-lookup"><span data-stu-id="f7efd-205">False</span></span>                                        |
| <span data-ttu-id="f7efd-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f7efd-206">Is-Single-Valued</span></span>       | <span data-ttu-id="f7efd-207">True</span><span class="sxs-lookup"><span data-stu-id="f7efd-207">True</span></span>                                         |
| <span data-ttu-id="f7efd-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="f7efd-208">Is Indexed</span></span>             | <span data-ttu-id="f7efd-209">Falso</span><span class="sxs-lookup"><span data-stu-id="f7efd-209">False</span></span>                                        |
| <span data-ttu-id="f7efd-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f7efd-210">In Global Catalog</span></span>      | <span data-ttu-id="f7efd-211">Falso</span><span class="sxs-lookup"><span data-stu-id="f7efd-211">False</span></span>                                        |
| <span data-ttu-id="f7efd-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f7efd-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7efd-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f7efd-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="f7efd-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7efd-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="f7efd-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7efd-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="f7efd-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7efd-216">Search-Flags</span></span>           | <span data-ttu-id="f7efd-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7efd-217">0x00000000</span></span>                                   |
| <span data-ttu-id="f7efd-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7efd-218">System-Flags</span></span>           | <span data-ttu-id="f7efd-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7efd-219">0x00000010</span></span>                                   |
| <span data-ttu-id="f7efd-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f7efd-220">Classes used in</span></span>        | [<span data-ttu-id="f7efd-221">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="f7efd-221">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f7efd-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f7efd-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f7efd-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7efd-223">Entry</span></span> | <span data-ttu-id="f7efd-224">Valor</span><span class="sxs-lookup"><span data-stu-id="f7efd-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="f7efd-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="f7efd-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="f7efd-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7efd-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="f7efd-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7efd-227">System-Only</span></span>            | <span data-ttu-id="f7efd-228">Falso</span><span class="sxs-lookup"><span data-stu-id="f7efd-228">False</span></span>                                        |
| <span data-ttu-id="f7efd-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f7efd-229">Is-Single-Valued</span></span>       | <span data-ttu-id="f7efd-230">True</span><span class="sxs-lookup"><span data-stu-id="f7efd-230">True</span></span>                                         |
| <span data-ttu-id="f7efd-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="f7efd-231">Is Indexed</span></span>             | <span data-ttu-id="f7efd-232">Falso</span><span class="sxs-lookup"><span data-stu-id="f7efd-232">False</span></span>                                        |
| <span data-ttu-id="f7efd-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f7efd-233">In Global Catalog</span></span>      | <span data-ttu-id="f7efd-234">Falso</span><span class="sxs-lookup"><span data-stu-id="f7efd-234">False</span></span>                                        |
| <span data-ttu-id="f7efd-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f7efd-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7efd-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f7efd-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="f7efd-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7efd-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="f7efd-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7efd-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="f7efd-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7efd-239">Search-Flags</span></span>           | <span data-ttu-id="f7efd-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7efd-240">0x00000000</span></span>                                   |
| <span data-ttu-id="f7efd-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7efd-241">System-Flags</span></span>           | <span data-ttu-id="f7efd-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7efd-242">0x00000010</span></span>                                   |
| <span data-ttu-id="f7efd-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f7efd-243">Classes used in</span></span>        | [<span data-ttu-id="f7efd-244">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="f7efd-244">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f7efd-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f7efd-245">Windows Server 2012</span></span>



| <span data-ttu-id="f7efd-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="f7efd-246">Entry</span></span> | <span data-ttu-id="f7efd-247">Valor</span><span class="sxs-lookup"><span data-stu-id="f7efd-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="f7efd-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="f7efd-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="f7efd-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7efd-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="f7efd-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7efd-250">System-Only</span></span>            | <span data-ttu-id="f7efd-251">Falso</span><span class="sxs-lookup"><span data-stu-id="f7efd-251">False</span></span>                                        |
| <span data-ttu-id="f7efd-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f7efd-252">Is-Single-Valued</span></span>       | <span data-ttu-id="f7efd-253">True</span><span class="sxs-lookup"><span data-stu-id="f7efd-253">True</span></span>                                         |
| <span data-ttu-id="f7efd-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="f7efd-254">Is Indexed</span></span>             | <span data-ttu-id="f7efd-255">Falso</span><span class="sxs-lookup"><span data-stu-id="f7efd-255">False</span></span>                                        |
| <span data-ttu-id="f7efd-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f7efd-256">In Global Catalog</span></span>      | <span data-ttu-id="f7efd-257">Falso</span><span class="sxs-lookup"><span data-stu-id="f7efd-257">False</span></span>                                        |
| <span data-ttu-id="f7efd-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f7efd-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7efd-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f7efd-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="f7efd-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7efd-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="f7efd-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7efd-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="f7efd-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7efd-262">Search-Flags</span></span>           | <span data-ttu-id="f7efd-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7efd-263">0x00000000</span></span>                                   |
| <span data-ttu-id="f7efd-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7efd-264">System-Flags</span></span>           | <span data-ttu-id="f7efd-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7efd-265">0x00000010</span></span>                                   |
| <span data-ttu-id="f7efd-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f7efd-266">Classes used in</span></span>        | [<span data-ttu-id="f7efd-267">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="f7efd-267">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 





