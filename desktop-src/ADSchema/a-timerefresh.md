---
title: Time-Refresh atributo
description: Esse atributo tem o intervalo durante o qual um registro de recurso contido em uma zona integrada Active Directory deve ser atualizado para o servidor DNS. O intervalo padrão é de 7 dias.
ms.assetid: 9e473c29-7fcf-4d6d-8a7c-2791c7822c7d
ms.tgt_platform: multiple
keywords:
- Esquema de Time-Refresh do atributo AD
- Esquema de AD do atributo timerefresh
topic_type:
- apiref
api_name:
- Time-Refresh
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87bc360686b1692d2dbda1ee23ad6351e69d3afe
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103919552"
---
# <a name="time-refresh-attribute"></a><span data-ttu-id="f5817-106">Time-Refresh atributo</span><span class="sxs-lookup"><span data-stu-id="f5817-106">Time-Refresh attribute</span></span>

<span data-ttu-id="f5817-107">Esse atributo tem o intervalo durante o qual um registro de recurso contido em uma zona integrada Active Directory deve ser atualizado para o servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="f5817-107">This attribute has the interval during which a resource record that is contained in an Active Directory integrated zone should be refreshed for the DNS server.</span></span> <span data-ttu-id="f5817-108">O intervalo padrão é de 7 dias.</span><span class="sxs-lookup"><span data-stu-id="f5817-108">The default interval is 7 days.</span></span>



| <span data-ttu-id="f5817-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5817-109">Entry</span></span> | <span data-ttu-id="f5817-110">Valor</span><span class="sxs-lookup"><span data-stu-id="f5817-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="f5817-111">CN</span><span class="sxs-lookup"><span data-stu-id="f5817-111">CN</span></span>                | <span data-ttu-id="f5817-112">Time-Refresh</span><span class="sxs-lookup"><span data-stu-id="f5817-112">Time-Refresh</span></span>                         |
| <span data-ttu-id="f5817-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f5817-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f5817-114">timerefresh</span><span class="sxs-lookup"><span data-stu-id="f5817-114">timeRefresh</span></span>                          |
| <span data-ttu-id="f5817-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="f5817-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="f5817-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="f5817-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="f5817-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="f5817-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="f5817-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f5817-118">Attribute-Id</span></span>      | <span data-ttu-id="f5817-119">1.2.840.113556.1.4.503</span><span class="sxs-lookup"><span data-stu-id="f5817-119">1.2.840.113556.1.4.503</span></span>               |
| <span data-ttu-id="f5817-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f5817-120">System-Id-Guid</span></span>    | <span data-ttu-id="f5817-121">ddac0cf1-af8f-11d0-afeb-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="f5817-121">ddac0cf1-af8f-11d0-afeb-00c04fd930c9</span></span> |
| <span data-ttu-id="f5817-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5817-122">Syntax</span></span>            | [<span data-ttu-id="f5817-123">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="f5817-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="f5817-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="f5817-124">Implementations</span></span>

-   [<span data-ttu-id="f5817-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f5817-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f5817-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f5817-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f5817-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f5817-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f5817-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f5817-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f5817-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f5817-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f5817-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f5817-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f5817-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f5817-131">Windows 2000 Server</span></span>



| <span data-ttu-id="f5817-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5817-132">Entry</span></span> | <span data-ttu-id="f5817-133">Valor</span><span class="sxs-lookup"><span data-stu-id="f5817-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5817-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="f5817-134">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="f5817-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f5817-135">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="f5817-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="f5817-136">System-Only</span></span>            | <span data-ttu-id="f5817-137">Falso</span><span class="sxs-lookup"><span data-stu-id="f5817-137">False</span></span>                                                                                                                         |
| <span data-ttu-id="f5817-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f5817-138">Is-Single-Valued</span></span>       | <span data-ttu-id="f5817-139">True</span><span class="sxs-lookup"><span data-stu-id="f5817-139">True</span></span>                                                                                                                          |
| <span data-ttu-id="f5817-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="f5817-140">Is Indexed</span></span>             | <span data-ttu-id="f5817-141">Falso</span><span class="sxs-lookup"><span data-stu-id="f5817-141">False</span></span>                                                                                                                         |
| <span data-ttu-id="f5817-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f5817-142">In Global Catalog</span></span>      | <span data-ttu-id="f5817-143">Falso</span><span class="sxs-lookup"><span data-stu-id="f5817-143">False</span></span>                                                                                                                         |
| <span data-ttu-id="f5817-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f5817-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="f5817-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f5817-145">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="f5817-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f5817-146">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="f5817-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f5817-147">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="f5817-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f5817-148">Search-Flags</span></span>           | <span data-ttu-id="f5817-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f5817-149">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="f5817-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f5817-150">System-Flags</span></span>           | <span data-ttu-id="f5817-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f5817-151">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="f5817-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f5817-152">Classes used in</span></span>        | [<span data-ttu-id="f5817-153">**Link-Track-OMT-entry**</span><span class="sxs-lookup"><span data-stu-id="f5817-153">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="f5817-154">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="f5817-154">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f5817-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f5817-155">Windows Server 2003</span></span>



| <span data-ttu-id="f5817-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5817-156">Entry</span></span> | <span data-ttu-id="f5817-157">Valor</span><span class="sxs-lookup"><span data-stu-id="f5817-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5817-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="f5817-158">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="f5817-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f5817-159">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="f5817-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="f5817-160">System-Only</span></span>            | <span data-ttu-id="f5817-161">Falso</span><span class="sxs-lookup"><span data-stu-id="f5817-161">False</span></span>                                                                                                                         |
| <span data-ttu-id="f5817-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f5817-162">Is-Single-Valued</span></span>       | <span data-ttu-id="f5817-163">True</span><span class="sxs-lookup"><span data-stu-id="f5817-163">True</span></span>                                                                                                                          |
| <span data-ttu-id="f5817-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="f5817-164">Is Indexed</span></span>             | <span data-ttu-id="f5817-165">Falso</span><span class="sxs-lookup"><span data-stu-id="f5817-165">False</span></span>                                                                                                                         |
| <span data-ttu-id="f5817-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f5817-166">In Global Catalog</span></span>      | <span data-ttu-id="f5817-167">Falso</span><span class="sxs-lookup"><span data-stu-id="f5817-167">False</span></span>                                                                                                                         |
| <span data-ttu-id="f5817-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f5817-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="f5817-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f5817-169">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="f5817-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f5817-170">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="f5817-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f5817-171">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="f5817-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f5817-172">Search-Flags</span></span>           | <span data-ttu-id="f5817-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f5817-173">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="f5817-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f5817-174">System-Flags</span></span>           | <span data-ttu-id="f5817-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f5817-175">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="f5817-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f5817-176">Classes used in</span></span>        | [<span data-ttu-id="f5817-177">**Link-Track-OMT-entry**</span><span class="sxs-lookup"><span data-stu-id="f5817-177">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="f5817-178">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="f5817-178">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f5817-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f5817-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f5817-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5817-180">Entry</span></span> | <span data-ttu-id="f5817-181">Valor</span><span class="sxs-lookup"><span data-stu-id="f5817-181">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5817-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="f5817-182">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="f5817-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f5817-183">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="f5817-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="f5817-184">System-Only</span></span>            | <span data-ttu-id="f5817-185">Falso</span><span class="sxs-lookup"><span data-stu-id="f5817-185">False</span></span>                                                                                                                         |
| <span data-ttu-id="f5817-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f5817-186">Is-Single-Valued</span></span>       | <span data-ttu-id="f5817-187">True</span><span class="sxs-lookup"><span data-stu-id="f5817-187">True</span></span>                                                                                                                          |
| <span data-ttu-id="f5817-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="f5817-188">Is Indexed</span></span>             | <span data-ttu-id="f5817-189">Falso</span><span class="sxs-lookup"><span data-stu-id="f5817-189">False</span></span>                                                                                                                         |
| <span data-ttu-id="f5817-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f5817-190">In Global Catalog</span></span>      | <span data-ttu-id="f5817-191">Falso</span><span class="sxs-lookup"><span data-stu-id="f5817-191">False</span></span>                                                                                                                         |
| <span data-ttu-id="f5817-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f5817-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="f5817-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f5817-193">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="f5817-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f5817-194">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="f5817-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f5817-195">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="f5817-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f5817-196">Search-Flags</span></span>           | <span data-ttu-id="f5817-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f5817-197">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="f5817-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f5817-198">System-Flags</span></span>           | <span data-ttu-id="f5817-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f5817-199">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="f5817-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f5817-200">Classes used in</span></span>        | [<span data-ttu-id="f5817-201">**Link-Track-OMT-entry**</span><span class="sxs-lookup"><span data-stu-id="f5817-201">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="f5817-202">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="f5817-202">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f5817-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f5817-203">Windows Server 2008</span></span>



| <span data-ttu-id="f5817-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5817-204">Entry</span></span> | <span data-ttu-id="f5817-205">Valor</span><span class="sxs-lookup"><span data-stu-id="f5817-205">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5817-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="f5817-206">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="f5817-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f5817-207">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="f5817-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="f5817-208">System-Only</span></span>            | <span data-ttu-id="f5817-209">Falso</span><span class="sxs-lookup"><span data-stu-id="f5817-209">False</span></span>                                                                                                                         |
| <span data-ttu-id="f5817-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f5817-210">Is-Single-Valued</span></span>       | <span data-ttu-id="f5817-211">True</span><span class="sxs-lookup"><span data-stu-id="f5817-211">True</span></span>                                                                                                                          |
| <span data-ttu-id="f5817-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="f5817-212">Is Indexed</span></span>             | <span data-ttu-id="f5817-213">Falso</span><span class="sxs-lookup"><span data-stu-id="f5817-213">False</span></span>                                                                                                                         |
| <span data-ttu-id="f5817-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f5817-214">In Global Catalog</span></span>      | <span data-ttu-id="f5817-215">Falso</span><span class="sxs-lookup"><span data-stu-id="f5817-215">False</span></span>                                                                                                                         |
| <span data-ttu-id="f5817-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f5817-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="f5817-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f5817-217">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="f5817-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f5817-218">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="f5817-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f5817-219">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="f5817-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f5817-220">Search-Flags</span></span>           | <span data-ttu-id="f5817-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f5817-221">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="f5817-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f5817-222">System-Flags</span></span>           | <span data-ttu-id="f5817-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f5817-223">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="f5817-224">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f5817-224">Classes used in</span></span>        | [<span data-ttu-id="f5817-225">**Link-Track-OMT-entry**</span><span class="sxs-lookup"><span data-stu-id="f5817-225">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="f5817-226">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="f5817-226">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f5817-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f5817-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f5817-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5817-228">Entry</span></span> | <span data-ttu-id="f5817-229">Valor</span><span class="sxs-lookup"><span data-stu-id="f5817-229">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5817-230">ID do link</span><span class="sxs-lookup"><span data-stu-id="f5817-230">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="f5817-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f5817-231">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="f5817-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="f5817-232">System-Only</span></span>            | <span data-ttu-id="f5817-233">Falso</span><span class="sxs-lookup"><span data-stu-id="f5817-233">False</span></span>                                                                                                                         |
| <span data-ttu-id="f5817-234">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f5817-234">Is-Single-Valued</span></span>       | <span data-ttu-id="f5817-235">True</span><span class="sxs-lookup"><span data-stu-id="f5817-235">True</span></span>                                                                                                                          |
| <span data-ttu-id="f5817-236">É indexado</span><span class="sxs-lookup"><span data-stu-id="f5817-236">Is Indexed</span></span>             | <span data-ttu-id="f5817-237">Falso</span><span class="sxs-lookup"><span data-stu-id="f5817-237">False</span></span>                                                                                                                         |
| <span data-ttu-id="f5817-238">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f5817-238">In Global Catalog</span></span>      | <span data-ttu-id="f5817-239">Falso</span><span class="sxs-lookup"><span data-stu-id="f5817-239">False</span></span>                                                                                                                         |
| <span data-ttu-id="f5817-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f5817-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="f5817-241">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f5817-241">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="f5817-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f5817-242">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="f5817-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f5817-243">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="f5817-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f5817-244">Search-Flags</span></span>           | <span data-ttu-id="f5817-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f5817-245">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="f5817-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f5817-246">System-Flags</span></span>           | <span data-ttu-id="f5817-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f5817-247">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="f5817-248">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f5817-248">Classes used in</span></span>        | [<span data-ttu-id="f5817-249">**Link-Track-OMT-entry**</span><span class="sxs-lookup"><span data-stu-id="f5817-249">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="f5817-250">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="f5817-250">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f5817-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f5817-251">Windows Server 2012</span></span>



| <span data-ttu-id="f5817-252">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5817-252">Entry</span></span> | <span data-ttu-id="f5817-253">Valor</span><span class="sxs-lookup"><span data-stu-id="f5817-253">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5817-254">ID do link</span><span class="sxs-lookup"><span data-stu-id="f5817-254">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="f5817-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f5817-255">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="f5817-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="f5817-256">System-Only</span></span>            | <span data-ttu-id="f5817-257">Falso</span><span class="sxs-lookup"><span data-stu-id="f5817-257">False</span></span>                                                                                                                         |
| <span data-ttu-id="f5817-258">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f5817-258">Is-Single-Valued</span></span>       | <span data-ttu-id="f5817-259">True</span><span class="sxs-lookup"><span data-stu-id="f5817-259">True</span></span>                                                                                                                          |
| <span data-ttu-id="f5817-260">É indexado</span><span class="sxs-lookup"><span data-stu-id="f5817-260">Is Indexed</span></span>             | <span data-ttu-id="f5817-261">Falso</span><span class="sxs-lookup"><span data-stu-id="f5817-261">False</span></span>                                                                                                                         |
| <span data-ttu-id="f5817-262">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f5817-262">In Global Catalog</span></span>      | <span data-ttu-id="f5817-263">Falso</span><span class="sxs-lookup"><span data-stu-id="f5817-263">False</span></span>                                                                                                                         |
| <span data-ttu-id="f5817-264">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f5817-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="f5817-265">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f5817-265">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="f5817-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f5817-266">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="f5817-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f5817-267">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="f5817-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f5817-268">Search-Flags</span></span>           | <span data-ttu-id="f5817-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f5817-269">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="f5817-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f5817-270">System-Flags</span></span>           | <span data-ttu-id="f5817-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f5817-271">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="f5817-272">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f5817-272">Classes used in</span></span>        | [<span data-ttu-id="f5817-273">**Link-Track-OMT-entry**</span><span class="sxs-lookup"><span data-stu-id="f5817-273">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="f5817-274">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="f5817-274">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



 

 





