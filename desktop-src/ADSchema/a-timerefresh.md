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
# <a name="time-refresh-attribute"></a><span data-ttu-id="27946-106">Time-Refresh atributo</span><span class="sxs-lookup"><span data-stu-id="27946-106">Time-Refresh attribute</span></span>

<span data-ttu-id="27946-107">Esse atributo tem o intervalo durante o qual um registro de recurso contido em uma zona integrada Active Directory deve ser atualizado para o servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="27946-107">This attribute has the interval during which a resource record that is contained in an Active Directory integrated zone should be refreshed for the DNS server.</span></span> <span data-ttu-id="27946-108">O intervalo padrão é de 7 dias.</span><span class="sxs-lookup"><span data-stu-id="27946-108">The default interval is 7 days.</span></span>



| <span data-ttu-id="27946-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="27946-109">Entry</span></span> | <span data-ttu-id="27946-110">Valor</span><span class="sxs-lookup"><span data-stu-id="27946-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="27946-111">CN</span><span class="sxs-lookup"><span data-stu-id="27946-111">CN</span></span>                | <span data-ttu-id="27946-112">Time-Refresh</span><span class="sxs-lookup"><span data-stu-id="27946-112">Time-Refresh</span></span>                         |
| <span data-ttu-id="27946-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="27946-113">Ldap-Display-Name</span></span> | <span data-ttu-id="27946-114">timerefresh</span><span class="sxs-lookup"><span data-stu-id="27946-114">timeRefresh</span></span>                          |
| <span data-ttu-id="27946-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="27946-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="27946-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="27946-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="27946-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="27946-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="27946-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="27946-118">Attribute-Id</span></span>      | <span data-ttu-id="27946-119">1.2.840.113556.1.4.503</span><span class="sxs-lookup"><span data-stu-id="27946-119">1.2.840.113556.1.4.503</span></span>               |
| <span data-ttu-id="27946-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="27946-120">System-Id-Guid</span></span>    | <span data-ttu-id="27946-121">ddac0cf1-af8f-11d0-afeb-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="27946-121">ddac0cf1-af8f-11d0-afeb-00c04fd930c9</span></span> |
| <span data-ttu-id="27946-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="27946-122">Syntax</span></span>            | [<span data-ttu-id="27946-123">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="27946-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="27946-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="27946-124">Implementations</span></span>

-   [<span data-ttu-id="27946-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="27946-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="27946-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="27946-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="27946-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="27946-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="27946-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="27946-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="27946-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="27946-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="27946-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="27946-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="27946-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="27946-131">Windows 2000 Server</span></span>



| <span data-ttu-id="27946-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="27946-132">Entry</span></span> | <span data-ttu-id="27946-133">Valor</span><span class="sxs-lookup"><span data-stu-id="27946-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27946-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="27946-134">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="27946-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27946-135">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="27946-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="27946-136">System-Only</span></span>            | <span data-ttu-id="27946-137">Falso</span><span class="sxs-lookup"><span data-stu-id="27946-137">False</span></span>                                                                                                                         |
| <span data-ttu-id="27946-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="27946-138">Is-Single-Valued</span></span>       | <span data-ttu-id="27946-139">True</span><span class="sxs-lookup"><span data-stu-id="27946-139">True</span></span>                                                                                                                          |
| <span data-ttu-id="27946-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="27946-140">Is Indexed</span></span>             | <span data-ttu-id="27946-141">Falso</span><span class="sxs-lookup"><span data-stu-id="27946-141">False</span></span>                                                                                                                         |
| <span data-ttu-id="27946-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="27946-142">In Global Catalog</span></span>      | <span data-ttu-id="27946-143">Falso</span><span class="sxs-lookup"><span data-stu-id="27946-143">False</span></span>                                                                                                                         |
| <span data-ttu-id="27946-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="27946-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="27946-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="27946-145">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="27946-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27946-146">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="27946-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27946-147">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="27946-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27946-148">Search-Flags</span></span>           | <span data-ttu-id="27946-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27946-149">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="27946-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27946-150">System-Flags</span></span>           | <span data-ttu-id="27946-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27946-151">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="27946-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="27946-152">Classes used in</span></span>        | [<span data-ttu-id="27946-153">**Link-Track-OMT-entry**</span><span class="sxs-lookup"><span data-stu-id="27946-153">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="27946-154">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="27946-154">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="27946-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="27946-155">Windows Server 2003</span></span>



| <span data-ttu-id="27946-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="27946-156">Entry</span></span> | <span data-ttu-id="27946-157">Valor</span><span class="sxs-lookup"><span data-stu-id="27946-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27946-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="27946-158">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="27946-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27946-159">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="27946-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="27946-160">System-Only</span></span>            | <span data-ttu-id="27946-161">Falso</span><span class="sxs-lookup"><span data-stu-id="27946-161">False</span></span>                                                                                                                         |
| <span data-ttu-id="27946-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="27946-162">Is-Single-Valued</span></span>       | <span data-ttu-id="27946-163">True</span><span class="sxs-lookup"><span data-stu-id="27946-163">True</span></span>                                                                                                                          |
| <span data-ttu-id="27946-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="27946-164">Is Indexed</span></span>             | <span data-ttu-id="27946-165">Falso</span><span class="sxs-lookup"><span data-stu-id="27946-165">False</span></span>                                                                                                                         |
| <span data-ttu-id="27946-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="27946-166">In Global Catalog</span></span>      | <span data-ttu-id="27946-167">Falso</span><span class="sxs-lookup"><span data-stu-id="27946-167">False</span></span>                                                                                                                         |
| <span data-ttu-id="27946-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="27946-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="27946-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="27946-169">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="27946-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27946-170">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="27946-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27946-171">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="27946-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27946-172">Search-Flags</span></span>           | <span data-ttu-id="27946-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27946-173">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="27946-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27946-174">System-Flags</span></span>           | <span data-ttu-id="27946-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27946-175">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="27946-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="27946-176">Classes used in</span></span>        | [<span data-ttu-id="27946-177">**Link-Track-OMT-entry**</span><span class="sxs-lookup"><span data-stu-id="27946-177">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="27946-178">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="27946-178">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="27946-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="27946-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="27946-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="27946-180">Entry</span></span> | <span data-ttu-id="27946-181">Valor</span><span class="sxs-lookup"><span data-stu-id="27946-181">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27946-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="27946-182">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="27946-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27946-183">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="27946-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="27946-184">System-Only</span></span>            | <span data-ttu-id="27946-185">Falso</span><span class="sxs-lookup"><span data-stu-id="27946-185">False</span></span>                                                                                                                         |
| <span data-ttu-id="27946-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="27946-186">Is-Single-Valued</span></span>       | <span data-ttu-id="27946-187">True</span><span class="sxs-lookup"><span data-stu-id="27946-187">True</span></span>                                                                                                                          |
| <span data-ttu-id="27946-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="27946-188">Is Indexed</span></span>             | <span data-ttu-id="27946-189">Falso</span><span class="sxs-lookup"><span data-stu-id="27946-189">False</span></span>                                                                                                                         |
| <span data-ttu-id="27946-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="27946-190">In Global Catalog</span></span>      | <span data-ttu-id="27946-191">Falso</span><span class="sxs-lookup"><span data-stu-id="27946-191">False</span></span>                                                                                                                         |
| <span data-ttu-id="27946-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="27946-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="27946-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="27946-193">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="27946-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27946-194">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="27946-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27946-195">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="27946-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27946-196">Search-Flags</span></span>           | <span data-ttu-id="27946-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27946-197">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="27946-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27946-198">System-Flags</span></span>           | <span data-ttu-id="27946-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27946-199">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="27946-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="27946-200">Classes used in</span></span>        | [<span data-ttu-id="27946-201">**Link-Track-OMT-entry**</span><span class="sxs-lookup"><span data-stu-id="27946-201">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="27946-202">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="27946-202">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="27946-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27946-203">Windows Server 2008</span></span>



| <span data-ttu-id="27946-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="27946-204">Entry</span></span> | <span data-ttu-id="27946-205">Valor</span><span class="sxs-lookup"><span data-stu-id="27946-205">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27946-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="27946-206">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="27946-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27946-207">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="27946-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="27946-208">System-Only</span></span>            | <span data-ttu-id="27946-209">Falso</span><span class="sxs-lookup"><span data-stu-id="27946-209">False</span></span>                                                                                                                         |
| <span data-ttu-id="27946-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="27946-210">Is-Single-Valued</span></span>       | <span data-ttu-id="27946-211">True</span><span class="sxs-lookup"><span data-stu-id="27946-211">True</span></span>                                                                                                                          |
| <span data-ttu-id="27946-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="27946-212">Is Indexed</span></span>             | <span data-ttu-id="27946-213">Falso</span><span class="sxs-lookup"><span data-stu-id="27946-213">False</span></span>                                                                                                                         |
| <span data-ttu-id="27946-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="27946-214">In Global Catalog</span></span>      | <span data-ttu-id="27946-215">Falso</span><span class="sxs-lookup"><span data-stu-id="27946-215">False</span></span>                                                                                                                         |
| <span data-ttu-id="27946-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="27946-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="27946-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="27946-217">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="27946-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27946-218">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="27946-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27946-219">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="27946-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27946-220">Search-Flags</span></span>           | <span data-ttu-id="27946-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27946-221">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="27946-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27946-222">System-Flags</span></span>           | <span data-ttu-id="27946-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27946-223">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="27946-224">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="27946-224">Classes used in</span></span>        | [<span data-ttu-id="27946-225">**Link-Track-OMT-entry**</span><span class="sxs-lookup"><span data-stu-id="27946-225">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="27946-226">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="27946-226">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="27946-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="27946-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="27946-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="27946-228">Entry</span></span> | <span data-ttu-id="27946-229">Valor</span><span class="sxs-lookup"><span data-stu-id="27946-229">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27946-230">ID do link</span><span class="sxs-lookup"><span data-stu-id="27946-230">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="27946-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27946-231">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="27946-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="27946-232">System-Only</span></span>            | <span data-ttu-id="27946-233">Falso</span><span class="sxs-lookup"><span data-stu-id="27946-233">False</span></span>                                                                                                                         |
| <span data-ttu-id="27946-234">É de valor único</span><span class="sxs-lookup"><span data-stu-id="27946-234">Is-Single-Valued</span></span>       | <span data-ttu-id="27946-235">True</span><span class="sxs-lookup"><span data-stu-id="27946-235">True</span></span>                                                                                                                          |
| <span data-ttu-id="27946-236">É indexado</span><span class="sxs-lookup"><span data-stu-id="27946-236">Is Indexed</span></span>             | <span data-ttu-id="27946-237">Falso</span><span class="sxs-lookup"><span data-stu-id="27946-237">False</span></span>                                                                                                                         |
| <span data-ttu-id="27946-238">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="27946-238">In Global Catalog</span></span>      | <span data-ttu-id="27946-239">Falso</span><span class="sxs-lookup"><span data-stu-id="27946-239">False</span></span>                                                                                                                         |
| <span data-ttu-id="27946-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="27946-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="27946-241">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="27946-241">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="27946-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27946-242">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="27946-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27946-243">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="27946-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27946-244">Search-Flags</span></span>           | <span data-ttu-id="27946-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27946-245">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="27946-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27946-246">System-Flags</span></span>           | <span data-ttu-id="27946-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27946-247">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="27946-248">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="27946-248">Classes used in</span></span>        | [<span data-ttu-id="27946-249">**Link-Track-OMT-entry**</span><span class="sxs-lookup"><span data-stu-id="27946-249">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="27946-250">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="27946-250">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="27946-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="27946-251">Windows Server 2012</span></span>



| <span data-ttu-id="27946-252">Entrada</span><span class="sxs-lookup"><span data-stu-id="27946-252">Entry</span></span> | <span data-ttu-id="27946-253">Valor</span><span class="sxs-lookup"><span data-stu-id="27946-253">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27946-254">ID do link</span><span class="sxs-lookup"><span data-stu-id="27946-254">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="27946-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27946-255">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="27946-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="27946-256">System-Only</span></span>            | <span data-ttu-id="27946-257">Falso</span><span class="sxs-lookup"><span data-stu-id="27946-257">False</span></span>                                                                                                                         |
| <span data-ttu-id="27946-258">É de valor único</span><span class="sxs-lookup"><span data-stu-id="27946-258">Is-Single-Valued</span></span>       | <span data-ttu-id="27946-259">True</span><span class="sxs-lookup"><span data-stu-id="27946-259">True</span></span>                                                                                                                          |
| <span data-ttu-id="27946-260">É indexado</span><span class="sxs-lookup"><span data-stu-id="27946-260">Is Indexed</span></span>             | <span data-ttu-id="27946-261">Falso</span><span class="sxs-lookup"><span data-stu-id="27946-261">False</span></span>                                                                                                                         |
| <span data-ttu-id="27946-262">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="27946-262">In Global Catalog</span></span>      | <span data-ttu-id="27946-263">Falso</span><span class="sxs-lookup"><span data-stu-id="27946-263">False</span></span>                                                                                                                         |
| <span data-ttu-id="27946-264">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="27946-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="27946-265">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="27946-265">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="27946-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27946-266">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="27946-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27946-267">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="27946-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27946-268">Search-Flags</span></span>           | <span data-ttu-id="27946-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27946-269">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="27946-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27946-270">System-Flags</span></span>           | <span data-ttu-id="27946-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27946-271">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="27946-272">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="27946-272">Classes used in</span></span>        | [<span data-ttu-id="27946-273">**Link-Track-OMT-entry**</span><span class="sxs-lookup"><span data-stu-id="27946-273">**Link-Track-OMT-Entry**</span></span>](c-linktrackomtentry.md)<br/> [<span data-ttu-id="27946-274">**Link-Track-Vol-entry**</span><span class="sxs-lookup"><span data-stu-id="27946-274">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



 

 





