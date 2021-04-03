---
title: ACS-atributo de nível de log de evento
description: Nível de log RSVP.
ms.assetid: 2f3c645d-a064-40fb-965c-388b2fac61bc
ms.tgt_platform: multiple
keywords:
- ACS-esquema de eventos no nível de log do evento do AD
- Esquema de AD do atributo aCSEventLogLevel
topic_type:
- apiref
api_name:
- ACS-Event-Log-Level
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62bb5701f665a3685845368eb2adc72fc33d10bd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645381"
---
# <a name="acs-event-log-level-attribute"></a><span data-ttu-id="ffb0f-105">ACS-atributo de nível de log de evento</span><span class="sxs-lookup"><span data-stu-id="ffb0f-105">ACS-Event-Log-Level attribute</span></span>

<span data-ttu-id="ffb0f-106">Nível de log RSVP.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-106">RSVP logging level.</span></span>



| <span data-ttu-id="ffb0f-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="ffb0f-107">Entry</span></span> | <span data-ttu-id="ffb0f-108">Valor</span><span class="sxs-lookup"><span data-stu-id="ffb0f-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="ffb0f-109">CN</span><span class="sxs-lookup"><span data-stu-id="ffb0f-109">CN</span></span>                | <span data-ttu-id="ffb0f-110">ACS-nível de log de eventos</span><span class="sxs-lookup"><span data-stu-id="ffb0f-110">ACS-Event-Log-Level</span></span>                     |
| <span data-ttu-id="ffb0f-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ffb0f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ffb0f-112">aCSEventLogLevel</span><span class="sxs-lookup"><span data-stu-id="ffb0f-112">aCSEventLogLevel</span></span>                        |
| <span data-ttu-id="ffb0f-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="ffb0f-113">Size</span></span>              | <span data-ttu-id="ffb0f-114">4 bytes pode ter os valores 0, 1, 2 e 3.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-114">4 bytes can have values 0, 1, 2, and 3.</span></span> |
| <span data-ttu-id="ffb0f-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="ffb0f-115">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="ffb0f-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="ffb0f-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="ffb0f-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ffb0f-117">Attribute-Id</span></span>      | <span data-ttu-id="ffb0f-118">1.2.840.113556.1.4.769</span><span class="sxs-lookup"><span data-stu-id="ffb0f-118">1.2.840.113556.1.4.769</span></span>                  |
| <span data-ttu-id="ffb0f-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ffb0f-119">System-Id-Guid</span></span>    | <span data-ttu-id="ffb0f-120">7f561286-5301-11d1-a9c5-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="ffb0f-120">7f561286-5301-11d1-a9c5-0000f80367c1</span></span>    |
| <span data-ttu-id="ffb0f-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffb0f-121">Syntax</span></span>            | [<span data-ttu-id="ffb0f-122">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="ffb0f-122">**Enumeration**</span></span>](s-enumeration.md)    |



## <a name="implementations"></a><span data-ttu-id="ffb0f-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="ffb0f-123">Implementations</span></span>

-   [<span data-ttu-id="ffb0f-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ffb0f-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ffb0f-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ffb0f-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ffb0f-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ffb0f-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ffb0f-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ffb0f-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ffb0f-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ffb0f-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ffb0f-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ffb0f-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ffb0f-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ffb0f-130">Windows 2000 Server</span></span>



| <span data-ttu-id="ffb0f-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="ffb0f-131">Entry</span></span> | <span data-ttu-id="ffb0f-132">Valor</span><span class="sxs-lookup"><span data-stu-id="ffb0f-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ffb0f-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="ffb0f-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ffb0f-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffb0f-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ffb0f-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffb0f-135">System-Only</span></span>            | <span data-ttu-id="ffb0f-136">Falso</span><span class="sxs-lookup"><span data-stu-id="ffb0f-136">False</span></span>                                        |
| <span data-ttu-id="ffb0f-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ffb0f-137">Is-Single-Valued</span></span>       | <span data-ttu-id="ffb0f-138">True</span><span class="sxs-lookup"><span data-stu-id="ffb0f-138">True</span></span>                                         |
| <span data-ttu-id="ffb0f-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="ffb0f-139">Is Indexed</span></span>             | <span data-ttu-id="ffb0f-140">Falso</span><span class="sxs-lookup"><span data-stu-id="ffb0f-140">False</span></span>                                        |
| <span data-ttu-id="ffb0f-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ffb0f-141">In Global Catalog</span></span>      | <span data-ttu-id="ffb0f-142">Falso</span><span class="sxs-lookup"><span data-stu-id="ffb0f-142">False</span></span>                                        |
| <span data-ttu-id="ffb0f-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ffb0f-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffb0f-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ffb0f-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ffb0f-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffb0f-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ffb0f-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffb0f-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ffb0f-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffb0f-147">Search-Flags</span></span>           | <span data-ttu-id="ffb0f-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ffb0f-148">0x00000000</span></span>                                   |
| <span data-ttu-id="ffb0f-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffb0f-149">System-Flags</span></span>           | <span data-ttu-id="ffb0f-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffb0f-150">0x00000010</span></span>                                   |
| <span data-ttu-id="ffb0f-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ffb0f-151">Classes used in</span></span>        | [<span data-ttu-id="ffb0f-152">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="ffb0f-152">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ffb0f-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ffb0f-153">Windows Server 2003</span></span>



| <span data-ttu-id="ffb0f-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="ffb0f-154">Entry</span></span> | <span data-ttu-id="ffb0f-155">Valor</span><span class="sxs-lookup"><span data-stu-id="ffb0f-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ffb0f-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="ffb0f-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ffb0f-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffb0f-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ffb0f-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffb0f-158">System-Only</span></span>            | <span data-ttu-id="ffb0f-159">Falso</span><span class="sxs-lookup"><span data-stu-id="ffb0f-159">False</span></span>                                        |
| <span data-ttu-id="ffb0f-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ffb0f-160">Is-Single-Valued</span></span>       | <span data-ttu-id="ffb0f-161">True</span><span class="sxs-lookup"><span data-stu-id="ffb0f-161">True</span></span>                                         |
| <span data-ttu-id="ffb0f-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="ffb0f-162">Is Indexed</span></span>             | <span data-ttu-id="ffb0f-163">Falso</span><span class="sxs-lookup"><span data-stu-id="ffb0f-163">False</span></span>                                        |
| <span data-ttu-id="ffb0f-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ffb0f-164">In Global Catalog</span></span>      | <span data-ttu-id="ffb0f-165">Falso</span><span class="sxs-lookup"><span data-stu-id="ffb0f-165">False</span></span>                                        |
| <span data-ttu-id="ffb0f-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ffb0f-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffb0f-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ffb0f-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ffb0f-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffb0f-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ffb0f-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffb0f-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ffb0f-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffb0f-170">Search-Flags</span></span>           | <span data-ttu-id="ffb0f-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ffb0f-171">0x00000000</span></span>                                   |
| <span data-ttu-id="ffb0f-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffb0f-172">System-Flags</span></span>           | <span data-ttu-id="ffb0f-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffb0f-173">0x00000010</span></span>                                   |
| <span data-ttu-id="ffb0f-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ffb0f-174">Classes used in</span></span>        | [<span data-ttu-id="ffb0f-175">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="ffb0f-175">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ffb0f-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ffb0f-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ffb0f-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="ffb0f-177">Entry</span></span> | <span data-ttu-id="ffb0f-178">Valor</span><span class="sxs-lookup"><span data-stu-id="ffb0f-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ffb0f-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="ffb0f-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ffb0f-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffb0f-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ffb0f-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffb0f-181">System-Only</span></span>            | <span data-ttu-id="ffb0f-182">Falso</span><span class="sxs-lookup"><span data-stu-id="ffb0f-182">False</span></span>                                        |
| <span data-ttu-id="ffb0f-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ffb0f-183">Is-Single-Valued</span></span>       | <span data-ttu-id="ffb0f-184">True</span><span class="sxs-lookup"><span data-stu-id="ffb0f-184">True</span></span>                                         |
| <span data-ttu-id="ffb0f-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="ffb0f-185">Is Indexed</span></span>             | <span data-ttu-id="ffb0f-186">Falso</span><span class="sxs-lookup"><span data-stu-id="ffb0f-186">False</span></span>                                        |
| <span data-ttu-id="ffb0f-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ffb0f-187">In Global Catalog</span></span>      | <span data-ttu-id="ffb0f-188">Falso</span><span class="sxs-lookup"><span data-stu-id="ffb0f-188">False</span></span>                                        |
| <span data-ttu-id="ffb0f-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ffb0f-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffb0f-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ffb0f-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ffb0f-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffb0f-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ffb0f-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffb0f-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ffb0f-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffb0f-193">Search-Flags</span></span>           | <span data-ttu-id="ffb0f-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ffb0f-194">0x00000000</span></span>                                   |
| <span data-ttu-id="ffb0f-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffb0f-195">System-Flags</span></span>           | <span data-ttu-id="ffb0f-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffb0f-196">0x00000010</span></span>                                   |
| <span data-ttu-id="ffb0f-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ffb0f-197">Classes used in</span></span>        | [<span data-ttu-id="ffb0f-198">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="ffb0f-198">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ffb0f-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ffb0f-199">Windows Server 2008</span></span>



| <span data-ttu-id="ffb0f-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="ffb0f-200">Entry</span></span> | <span data-ttu-id="ffb0f-201">Valor</span><span class="sxs-lookup"><span data-stu-id="ffb0f-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ffb0f-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="ffb0f-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ffb0f-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffb0f-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ffb0f-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffb0f-204">System-Only</span></span>            | <span data-ttu-id="ffb0f-205">Falso</span><span class="sxs-lookup"><span data-stu-id="ffb0f-205">False</span></span>                                        |
| <span data-ttu-id="ffb0f-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ffb0f-206">Is-Single-Valued</span></span>       | <span data-ttu-id="ffb0f-207">True</span><span class="sxs-lookup"><span data-stu-id="ffb0f-207">True</span></span>                                         |
| <span data-ttu-id="ffb0f-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="ffb0f-208">Is Indexed</span></span>             | <span data-ttu-id="ffb0f-209">Falso</span><span class="sxs-lookup"><span data-stu-id="ffb0f-209">False</span></span>                                        |
| <span data-ttu-id="ffb0f-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ffb0f-210">In Global Catalog</span></span>      | <span data-ttu-id="ffb0f-211">Falso</span><span class="sxs-lookup"><span data-stu-id="ffb0f-211">False</span></span>                                        |
| <span data-ttu-id="ffb0f-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ffb0f-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffb0f-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ffb0f-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ffb0f-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffb0f-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ffb0f-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffb0f-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ffb0f-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffb0f-216">Search-Flags</span></span>           | <span data-ttu-id="ffb0f-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ffb0f-217">0x00000000</span></span>                                   |
| <span data-ttu-id="ffb0f-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffb0f-218">System-Flags</span></span>           | <span data-ttu-id="ffb0f-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffb0f-219">0x00000010</span></span>                                   |
| <span data-ttu-id="ffb0f-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ffb0f-220">Classes used in</span></span>        | [<span data-ttu-id="ffb0f-221">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="ffb0f-221">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ffb0f-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ffb0f-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ffb0f-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="ffb0f-223">Entry</span></span> | <span data-ttu-id="ffb0f-224">Valor</span><span class="sxs-lookup"><span data-stu-id="ffb0f-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ffb0f-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="ffb0f-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ffb0f-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffb0f-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ffb0f-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffb0f-227">System-Only</span></span>            | <span data-ttu-id="ffb0f-228">Falso</span><span class="sxs-lookup"><span data-stu-id="ffb0f-228">False</span></span>                                        |
| <span data-ttu-id="ffb0f-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ffb0f-229">Is-Single-Valued</span></span>       | <span data-ttu-id="ffb0f-230">True</span><span class="sxs-lookup"><span data-stu-id="ffb0f-230">True</span></span>                                         |
| <span data-ttu-id="ffb0f-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="ffb0f-231">Is Indexed</span></span>             | <span data-ttu-id="ffb0f-232">Falso</span><span class="sxs-lookup"><span data-stu-id="ffb0f-232">False</span></span>                                        |
| <span data-ttu-id="ffb0f-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ffb0f-233">In Global Catalog</span></span>      | <span data-ttu-id="ffb0f-234">Falso</span><span class="sxs-lookup"><span data-stu-id="ffb0f-234">False</span></span>                                        |
| <span data-ttu-id="ffb0f-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ffb0f-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffb0f-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ffb0f-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ffb0f-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffb0f-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ffb0f-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffb0f-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ffb0f-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffb0f-239">Search-Flags</span></span>           | <span data-ttu-id="ffb0f-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ffb0f-240">0x00000000</span></span>                                   |
| <span data-ttu-id="ffb0f-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffb0f-241">System-Flags</span></span>           | <span data-ttu-id="ffb0f-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffb0f-242">0x00000010</span></span>                                   |
| <span data-ttu-id="ffb0f-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ffb0f-243">Classes used in</span></span>        | [<span data-ttu-id="ffb0f-244">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="ffb0f-244">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ffb0f-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ffb0f-245">Windows Server 2012</span></span>



| <span data-ttu-id="ffb0f-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="ffb0f-246">Entry</span></span> | <span data-ttu-id="ffb0f-247">Valor</span><span class="sxs-lookup"><span data-stu-id="ffb0f-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ffb0f-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="ffb0f-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ffb0f-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffb0f-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ffb0f-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffb0f-250">System-Only</span></span>            | <span data-ttu-id="ffb0f-251">Falso</span><span class="sxs-lookup"><span data-stu-id="ffb0f-251">False</span></span>                                        |
| <span data-ttu-id="ffb0f-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ffb0f-252">Is-Single-Valued</span></span>       | <span data-ttu-id="ffb0f-253">True</span><span class="sxs-lookup"><span data-stu-id="ffb0f-253">True</span></span>                                         |
| <span data-ttu-id="ffb0f-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="ffb0f-254">Is Indexed</span></span>             | <span data-ttu-id="ffb0f-255">Falso</span><span class="sxs-lookup"><span data-stu-id="ffb0f-255">False</span></span>                                        |
| <span data-ttu-id="ffb0f-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ffb0f-256">In Global Catalog</span></span>      | <span data-ttu-id="ffb0f-257">Falso</span><span class="sxs-lookup"><span data-stu-id="ffb0f-257">False</span></span>                                        |
| <span data-ttu-id="ffb0f-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ffb0f-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffb0f-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ffb0f-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ffb0f-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffb0f-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ffb0f-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffb0f-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ffb0f-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffb0f-262">Search-Flags</span></span>           | <span data-ttu-id="ffb0f-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ffb0f-263">0x00000000</span></span>                                   |
| <span data-ttu-id="ffb0f-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffb0f-264">System-Flags</span></span>           | <span data-ttu-id="ffb0f-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffb0f-265">0x00000010</span></span>                                   |
| <span data-ttu-id="ffb0f-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ffb0f-266">Classes used in</span></span>        | [<span data-ttu-id="ffb0f-267">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="ffb0f-267">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





