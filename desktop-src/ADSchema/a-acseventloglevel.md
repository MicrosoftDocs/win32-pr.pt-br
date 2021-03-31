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
# <a name="acs-event-log-level-attribute"></a><span data-ttu-id="dfb94-105">ACS-atributo de nível de log de evento</span><span class="sxs-lookup"><span data-stu-id="dfb94-105">ACS-Event-Log-Level attribute</span></span>

<span data-ttu-id="dfb94-106">Nível de log RSVP.</span><span class="sxs-lookup"><span data-stu-id="dfb94-106">RSVP logging level.</span></span>



| <span data-ttu-id="dfb94-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="dfb94-107">Entry</span></span> | <span data-ttu-id="dfb94-108">Valor</span><span class="sxs-lookup"><span data-stu-id="dfb94-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="dfb94-109">CN</span><span class="sxs-lookup"><span data-stu-id="dfb94-109">CN</span></span>                | <span data-ttu-id="dfb94-110">ACS-nível de log de eventos</span><span class="sxs-lookup"><span data-stu-id="dfb94-110">ACS-Event-Log-Level</span></span>                     |
| <span data-ttu-id="dfb94-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="dfb94-111">Ldap-Display-Name</span></span> | <span data-ttu-id="dfb94-112">aCSEventLogLevel</span><span class="sxs-lookup"><span data-stu-id="dfb94-112">aCSEventLogLevel</span></span>                        |
| <span data-ttu-id="dfb94-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="dfb94-113">Size</span></span>              | <span data-ttu-id="dfb94-114">4 bytes pode ter os valores 0, 1, 2 e 3.</span><span class="sxs-lookup"><span data-stu-id="dfb94-114">4 bytes can have values 0, 1, 2, and 3.</span></span> |
| <span data-ttu-id="dfb94-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="dfb94-115">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="dfb94-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="dfb94-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="dfb94-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="dfb94-117">Attribute-Id</span></span>      | <span data-ttu-id="dfb94-118">1.2.840.113556.1.4.769</span><span class="sxs-lookup"><span data-stu-id="dfb94-118">1.2.840.113556.1.4.769</span></span>                  |
| <span data-ttu-id="dfb94-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="dfb94-119">System-Id-Guid</span></span>    | <span data-ttu-id="dfb94-120">7f561286-5301-11d1-a9c5-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="dfb94-120">7f561286-5301-11d1-a9c5-0000f80367c1</span></span>    |
| <span data-ttu-id="dfb94-121">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dfb94-121">Syntax</span></span>            | [<span data-ttu-id="dfb94-122">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="dfb94-122">**Enumeration**</span></span>](s-enumeration.md)    |



## <a name="implementations"></a><span data-ttu-id="dfb94-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="dfb94-123">Implementations</span></span>

-   [<span data-ttu-id="dfb94-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="dfb94-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="dfb94-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="dfb94-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="dfb94-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="dfb94-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="dfb94-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="dfb94-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="dfb94-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="dfb94-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="dfb94-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="dfb94-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="dfb94-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dfb94-130">Windows 2000 Server</span></span>



| <span data-ttu-id="dfb94-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="dfb94-131">Entry</span></span> | <span data-ttu-id="dfb94-132">Valor</span><span class="sxs-lookup"><span data-stu-id="dfb94-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="dfb94-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="dfb94-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="dfb94-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dfb94-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="dfb94-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="dfb94-135">System-Only</span></span>            | <span data-ttu-id="dfb94-136">Falso</span><span class="sxs-lookup"><span data-stu-id="dfb94-136">False</span></span>                                        |
| <span data-ttu-id="dfb94-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="dfb94-137">Is-Single-Valued</span></span>       | <span data-ttu-id="dfb94-138">True</span><span class="sxs-lookup"><span data-stu-id="dfb94-138">True</span></span>                                         |
| <span data-ttu-id="dfb94-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="dfb94-139">Is Indexed</span></span>             | <span data-ttu-id="dfb94-140">Falso</span><span class="sxs-lookup"><span data-stu-id="dfb94-140">False</span></span>                                        |
| <span data-ttu-id="dfb94-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="dfb94-141">In Global Catalog</span></span>      | <span data-ttu-id="dfb94-142">Falso</span><span class="sxs-lookup"><span data-stu-id="dfb94-142">False</span></span>                                        |
| <span data-ttu-id="dfb94-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dfb94-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="dfb94-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="dfb94-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="dfb94-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dfb94-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="dfb94-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dfb94-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="dfb94-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dfb94-147">Search-Flags</span></span>           | <span data-ttu-id="dfb94-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dfb94-148">0x00000000</span></span>                                   |
| <span data-ttu-id="dfb94-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dfb94-149">System-Flags</span></span>           | <span data-ttu-id="dfb94-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dfb94-150">0x00000010</span></span>                                   |
| <span data-ttu-id="dfb94-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="dfb94-151">Classes used in</span></span>        | [<span data-ttu-id="dfb94-152">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="dfb94-152">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="dfb94-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dfb94-153">Windows Server 2003</span></span>



| <span data-ttu-id="dfb94-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="dfb94-154">Entry</span></span> | <span data-ttu-id="dfb94-155">Valor</span><span class="sxs-lookup"><span data-stu-id="dfb94-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="dfb94-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="dfb94-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="dfb94-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dfb94-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="dfb94-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="dfb94-158">System-Only</span></span>            | <span data-ttu-id="dfb94-159">Falso</span><span class="sxs-lookup"><span data-stu-id="dfb94-159">False</span></span>                                        |
| <span data-ttu-id="dfb94-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="dfb94-160">Is-Single-Valued</span></span>       | <span data-ttu-id="dfb94-161">True</span><span class="sxs-lookup"><span data-stu-id="dfb94-161">True</span></span>                                         |
| <span data-ttu-id="dfb94-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="dfb94-162">Is Indexed</span></span>             | <span data-ttu-id="dfb94-163">Falso</span><span class="sxs-lookup"><span data-stu-id="dfb94-163">False</span></span>                                        |
| <span data-ttu-id="dfb94-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="dfb94-164">In Global Catalog</span></span>      | <span data-ttu-id="dfb94-165">Falso</span><span class="sxs-lookup"><span data-stu-id="dfb94-165">False</span></span>                                        |
| <span data-ttu-id="dfb94-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dfb94-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="dfb94-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="dfb94-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="dfb94-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dfb94-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="dfb94-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dfb94-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="dfb94-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dfb94-170">Search-Flags</span></span>           | <span data-ttu-id="dfb94-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dfb94-171">0x00000000</span></span>                                   |
| <span data-ttu-id="dfb94-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dfb94-172">System-Flags</span></span>           | <span data-ttu-id="dfb94-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dfb94-173">0x00000010</span></span>                                   |
| <span data-ttu-id="dfb94-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="dfb94-174">Classes used in</span></span>        | [<span data-ttu-id="dfb94-175">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="dfb94-175">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="dfb94-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="dfb94-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="dfb94-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="dfb94-177">Entry</span></span> | <span data-ttu-id="dfb94-178">Valor</span><span class="sxs-lookup"><span data-stu-id="dfb94-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="dfb94-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="dfb94-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="dfb94-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dfb94-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="dfb94-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="dfb94-181">System-Only</span></span>            | <span data-ttu-id="dfb94-182">Falso</span><span class="sxs-lookup"><span data-stu-id="dfb94-182">False</span></span>                                        |
| <span data-ttu-id="dfb94-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="dfb94-183">Is-Single-Valued</span></span>       | <span data-ttu-id="dfb94-184">True</span><span class="sxs-lookup"><span data-stu-id="dfb94-184">True</span></span>                                         |
| <span data-ttu-id="dfb94-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="dfb94-185">Is Indexed</span></span>             | <span data-ttu-id="dfb94-186">Falso</span><span class="sxs-lookup"><span data-stu-id="dfb94-186">False</span></span>                                        |
| <span data-ttu-id="dfb94-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="dfb94-187">In Global Catalog</span></span>      | <span data-ttu-id="dfb94-188">Falso</span><span class="sxs-lookup"><span data-stu-id="dfb94-188">False</span></span>                                        |
| <span data-ttu-id="dfb94-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dfb94-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="dfb94-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="dfb94-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="dfb94-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dfb94-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="dfb94-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dfb94-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="dfb94-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dfb94-193">Search-Flags</span></span>           | <span data-ttu-id="dfb94-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dfb94-194">0x00000000</span></span>                                   |
| <span data-ttu-id="dfb94-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dfb94-195">System-Flags</span></span>           | <span data-ttu-id="dfb94-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dfb94-196">0x00000010</span></span>                                   |
| <span data-ttu-id="dfb94-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="dfb94-197">Classes used in</span></span>        | [<span data-ttu-id="dfb94-198">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="dfb94-198">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="dfb94-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dfb94-199">Windows Server 2008</span></span>



| <span data-ttu-id="dfb94-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="dfb94-200">Entry</span></span> | <span data-ttu-id="dfb94-201">Valor</span><span class="sxs-lookup"><span data-stu-id="dfb94-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="dfb94-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="dfb94-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="dfb94-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dfb94-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="dfb94-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="dfb94-204">System-Only</span></span>            | <span data-ttu-id="dfb94-205">Falso</span><span class="sxs-lookup"><span data-stu-id="dfb94-205">False</span></span>                                        |
| <span data-ttu-id="dfb94-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="dfb94-206">Is-Single-Valued</span></span>       | <span data-ttu-id="dfb94-207">True</span><span class="sxs-lookup"><span data-stu-id="dfb94-207">True</span></span>                                         |
| <span data-ttu-id="dfb94-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="dfb94-208">Is Indexed</span></span>             | <span data-ttu-id="dfb94-209">Falso</span><span class="sxs-lookup"><span data-stu-id="dfb94-209">False</span></span>                                        |
| <span data-ttu-id="dfb94-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="dfb94-210">In Global Catalog</span></span>      | <span data-ttu-id="dfb94-211">Falso</span><span class="sxs-lookup"><span data-stu-id="dfb94-211">False</span></span>                                        |
| <span data-ttu-id="dfb94-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dfb94-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="dfb94-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="dfb94-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="dfb94-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dfb94-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="dfb94-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dfb94-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="dfb94-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dfb94-216">Search-Flags</span></span>           | <span data-ttu-id="dfb94-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dfb94-217">0x00000000</span></span>                                   |
| <span data-ttu-id="dfb94-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dfb94-218">System-Flags</span></span>           | <span data-ttu-id="dfb94-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dfb94-219">0x00000010</span></span>                                   |
| <span data-ttu-id="dfb94-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="dfb94-220">Classes used in</span></span>        | [<span data-ttu-id="dfb94-221">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="dfb94-221">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="dfb94-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dfb94-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="dfb94-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="dfb94-223">Entry</span></span> | <span data-ttu-id="dfb94-224">Valor</span><span class="sxs-lookup"><span data-stu-id="dfb94-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="dfb94-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="dfb94-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="dfb94-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dfb94-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="dfb94-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="dfb94-227">System-Only</span></span>            | <span data-ttu-id="dfb94-228">Falso</span><span class="sxs-lookup"><span data-stu-id="dfb94-228">False</span></span>                                        |
| <span data-ttu-id="dfb94-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="dfb94-229">Is-Single-Valued</span></span>       | <span data-ttu-id="dfb94-230">True</span><span class="sxs-lookup"><span data-stu-id="dfb94-230">True</span></span>                                         |
| <span data-ttu-id="dfb94-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="dfb94-231">Is Indexed</span></span>             | <span data-ttu-id="dfb94-232">Falso</span><span class="sxs-lookup"><span data-stu-id="dfb94-232">False</span></span>                                        |
| <span data-ttu-id="dfb94-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="dfb94-233">In Global Catalog</span></span>      | <span data-ttu-id="dfb94-234">Falso</span><span class="sxs-lookup"><span data-stu-id="dfb94-234">False</span></span>                                        |
| <span data-ttu-id="dfb94-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dfb94-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="dfb94-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="dfb94-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="dfb94-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dfb94-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="dfb94-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dfb94-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="dfb94-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dfb94-239">Search-Flags</span></span>           | <span data-ttu-id="dfb94-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dfb94-240">0x00000000</span></span>                                   |
| <span data-ttu-id="dfb94-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dfb94-241">System-Flags</span></span>           | <span data-ttu-id="dfb94-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dfb94-242">0x00000010</span></span>                                   |
| <span data-ttu-id="dfb94-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="dfb94-243">Classes used in</span></span>        | [<span data-ttu-id="dfb94-244">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="dfb94-244">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="dfb94-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dfb94-245">Windows Server 2012</span></span>



| <span data-ttu-id="dfb94-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="dfb94-246">Entry</span></span> | <span data-ttu-id="dfb94-247">Valor</span><span class="sxs-lookup"><span data-stu-id="dfb94-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="dfb94-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="dfb94-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="dfb94-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dfb94-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="dfb94-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="dfb94-250">System-Only</span></span>            | <span data-ttu-id="dfb94-251">Falso</span><span class="sxs-lookup"><span data-stu-id="dfb94-251">False</span></span>                                        |
| <span data-ttu-id="dfb94-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="dfb94-252">Is-Single-Valued</span></span>       | <span data-ttu-id="dfb94-253">True</span><span class="sxs-lookup"><span data-stu-id="dfb94-253">True</span></span>                                         |
| <span data-ttu-id="dfb94-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="dfb94-254">Is Indexed</span></span>             | <span data-ttu-id="dfb94-255">Falso</span><span class="sxs-lookup"><span data-stu-id="dfb94-255">False</span></span>                                        |
| <span data-ttu-id="dfb94-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="dfb94-256">In Global Catalog</span></span>      | <span data-ttu-id="dfb94-257">Falso</span><span class="sxs-lookup"><span data-stu-id="dfb94-257">False</span></span>                                        |
| <span data-ttu-id="dfb94-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dfb94-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="dfb94-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="dfb94-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="dfb94-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dfb94-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="dfb94-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dfb94-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="dfb94-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dfb94-262">Search-Flags</span></span>           | <span data-ttu-id="dfb94-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dfb94-263">0x00000000</span></span>                                   |
| <span data-ttu-id="dfb94-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dfb94-264">System-Flags</span></span>           | <span data-ttu-id="dfb94-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dfb94-265">0x00000010</span></span>                                   |
| <span data-ttu-id="dfb94-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="dfb94-266">Classes used in</span></span>        | [<span data-ttu-id="dfb94-267">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="dfb94-267">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





