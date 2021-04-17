---
title: Coll-atributo de período de lixo
description: Esse atributo está localizado no serviço de diretório CN, CN Windows NT, serviços CN, configuração CN,... objeto. Ele representa o tempo, em horas, entre as execuções de coleta de lixo DS.
ms.assetid: 982a75f9-04b5-489e-99b3-a9fd3fb280c8
ms.tgt_platform: multiple
keywords:
- Coll-esquema de AD do atributo de período de lixo
- Esquema de AD do atributo garbageCollPeriod
topic_type:
- apiref
api_name:
- Garbage-Coll-Period
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64890df97cf4c131ad0dcdbed8cb80bf20b66a83
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105755257"
---
# <a name="garbage-coll-period-attribute"></a><span data-ttu-id="6c961-106">Coll-atributo de período de lixo</span><span class="sxs-lookup"><span data-stu-id="6c961-106">Garbage-Coll-Period attribute</span></span>

<span data-ttu-id="6c961-107">Esse atributo está localizado em CN = serviço de diretório, CN = Windows NT, CN = Services, CN = Configuration,... objeto.</span><span class="sxs-lookup"><span data-stu-id="6c961-107">This attribute is located on the CN=Directory Service,CN=Windows NT,CN=Services,CN=Configuration,... object.</span></span> <span data-ttu-id="6c961-108">Ele representa o tempo, em horas, entre as execuções de coleta de lixo DS.</span><span class="sxs-lookup"><span data-stu-id="6c961-108">It represents the time, in hours, between DS garbage collection runs.</span></span>



| <span data-ttu-id="6c961-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c961-109">Entry</span></span> | <span data-ttu-id="6c961-110">Valor</span><span class="sxs-lookup"><span data-stu-id="6c961-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="6c961-111">CN</span><span class="sxs-lookup"><span data-stu-id="6c961-111">CN</span></span>                | <span data-ttu-id="6c961-112">Lixo-Coll-period</span><span class="sxs-lookup"><span data-stu-id="6c961-112">Garbage-Coll-Period</span></span>                  |
| <span data-ttu-id="6c961-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6c961-113">Ldap-Display-Name</span></span> | <span data-ttu-id="6c961-114">garbageCollPeriod</span><span class="sxs-lookup"><span data-stu-id="6c961-114">garbageCollPeriod</span></span>                    |
| <span data-ttu-id="6c961-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="6c961-115">Size</span></span>              | <span data-ttu-id="6c961-116">4 bytes</span><span class="sxs-lookup"><span data-stu-id="6c961-116">4 bytes</span></span>                              |
| <span data-ttu-id="6c961-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="6c961-117">Update Privilege</span></span>  | <span data-ttu-id="6c961-118">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="6c961-118">Domain administrator</span></span>                 |
| <span data-ttu-id="6c961-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="6c961-119">Update Frequency</span></span>  | <span data-ttu-id="6c961-120">Muito raro.</span><span class="sxs-lookup"><span data-stu-id="6c961-120">Very rare.</span></span>                           |
| <span data-ttu-id="6c961-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6c961-121">Attribute-Id</span></span>      | <span data-ttu-id="6c961-122">1.2.840.113556.1.2.301</span><span class="sxs-lookup"><span data-stu-id="6c961-122">1.2.840.113556.1.2.301</span></span>               |
| <span data-ttu-id="6c961-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6c961-123">System-Id-Guid</span></span>    | <span data-ttu-id="6c961-124">5fd424a1-1262-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="6c961-124">5fd424a1-1262-11d0-a060-00aa006c33ed</span></span> |
| <span data-ttu-id="6c961-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c961-125">Syntax</span></span>            | [<span data-ttu-id="6c961-126">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="6c961-126">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="6c961-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="6c961-127">Implementations</span></span>

-   [<span data-ttu-id="6c961-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6c961-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6c961-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6c961-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6c961-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="6c961-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6c961-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6c961-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6c961-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6c961-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6c961-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6c961-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6c961-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6c961-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6c961-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6c961-135">Windows 2000 Server</span></span>



| <span data-ttu-id="6c961-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c961-136">Entry</span></span> | <span data-ttu-id="6c961-137">Valor</span><span class="sxs-lookup"><span data-stu-id="6c961-137">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c961-138">ID do link</span><span class="sxs-lookup"><span data-stu-id="6c961-138">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="6c961-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c961-139">MAPI-Id</span></span>                | <span data-ttu-id="6c961-140">0x80AF</span><span class="sxs-lookup"><span data-stu-id="6c961-140">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="6c961-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c961-141">System-Only</span></span>            | <span data-ttu-id="6c961-142">Falso</span><span class="sxs-lookup"><span data-stu-id="6c961-142">False</span></span>                                                                                                 |
| <span data-ttu-id="6c961-143">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6c961-143">Is-Single-Valued</span></span>       | <span data-ttu-id="6c961-144">True</span><span class="sxs-lookup"><span data-stu-id="6c961-144">True</span></span>                                                                                                  |
| <span data-ttu-id="6c961-145">É indexado</span><span class="sxs-lookup"><span data-stu-id="6c961-145">Is Indexed</span></span>             | <span data-ttu-id="6c961-146">Falso</span><span class="sxs-lookup"><span data-stu-id="6c961-146">False</span></span>                                                                                                 |
| <span data-ttu-id="6c961-147">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6c961-147">In Global Catalog</span></span>      | <span data-ttu-id="6c961-148">Falso</span><span class="sxs-lookup"><span data-stu-id="6c961-148">False</span></span>                                                                                                 |
| <span data-ttu-id="6c961-149">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6c961-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c961-150">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6c961-150">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="6c961-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c961-151">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="6c961-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c961-152">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="6c961-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c961-153">Search-Flags</span></span>           | <span data-ttu-id="6c961-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c961-154">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="6c961-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c961-155">System-Flags</span></span>           | <span data-ttu-id="6c961-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c961-156">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="6c961-157">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6c961-157">Classes used in</span></span>        | [<span data-ttu-id="6c961-158">**Destinatário de email**</span><span class="sxs-lookup"><span data-stu-id="6c961-158">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="6c961-159">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="6c961-159">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6c961-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6c961-160">Windows Server 2003</span></span>



| <span data-ttu-id="6c961-161">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c961-161">Entry</span></span> | <span data-ttu-id="6c961-162">Valor</span><span class="sxs-lookup"><span data-stu-id="6c961-162">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c961-163">ID do link</span><span class="sxs-lookup"><span data-stu-id="6c961-163">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="6c961-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c961-164">MAPI-Id</span></span>                | <span data-ttu-id="6c961-165">0x80AF</span><span class="sxs-lookup"><span data-stu-id="6c961-165">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="6c961-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c961-166">System-Only</span></span>            | <span data-ttu-id="6c961-167">Falso</span><span class="sxs-lookup"><span data-stu-id="6c961-167">False</span></span>                                                                                                 |
| <span data-ttu-id="6c961-168">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6c961-168">Is-Single-Valued</span></span>       | <span data-ttu-id="6c961-169">True</span><span class="sxs-lookup"><span data-stu-id="6c961-169">True</span></span>                                                                                                  |
| <span data-ttu-id="6c961-170">É indexado</span><span class="sxs-lookup"><span data-stu-id="6c961-170">Is Indexed</span></span>             | <span data-ttu-id="6c961-171">Falso</span><span class="sxs-lookup"><span data-stu-id="6c961-171">False</span></span>                                                                                                 |
| <span data-ttu-id="6c961-172">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6c961-172">In Global Catalog</span></span>      | <span data-ttu-id="6c961-173">Falso</span><span class="sxs-lookup"><span data-stu-id="6c961-173">False</span></span>                                                                                                 |
| <span data-ttu-id="6c961-174">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6c961-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c961-175">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6c961-175">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="6c961-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c961-176">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="6c961-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c961-177">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="6c961-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c961-178">Search-Flags</span></span>           | <span data-ttu-id="6c961-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c961-179">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="6c961-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c961-180">System-Flags</span></span>           | <span data-ttu-id="6c961-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c961-181">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="6c961-182">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6c961-182">Classes used in</span></span>        | [<span data-ttu-id="6c961-183">**Destinatário de email**</span><span class="sxs-lookup"><span data-stu-id="6c961-183">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="6c961-184">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="6c961-184">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6c961-185">ADAM</span><span class="sxs-lookup"><span data-stu-id="6c961-185">ADAM</span></span>



| <span data-ttu-id="6c961-186">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c961-186">Entry</span></span> | <span data-ttu-id="6c961-187">Valor</span><span class="sxs-lookup"><span data-stu-id="6c961-187">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="6c961-188">ID do link</span><span class="sxs-lookup"><span data-stu-id="6c961-188">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="6c961-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c961-189">MAPI-Id</span></span>                | <span data-ttu-id="6c961-190">0x80AF</span><span class="sxs-lookup"><span data-stu-id="6c961-190">0x80AF</span></span>                                           |
| <span data-ttu-id="6c961-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c961-191">System-Only</span></span>            | <span data-ttu-id="6c961-192">Falso</span><span class="sxs-lookup"><span data-stu-id="6c961-192">False</span></span>                                            |
| <span data-ttu-id="6c961-193">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6c961-193">Is-Single-Valued</span></span>       | <span data-ttu-id="6c961-194">True</span><span class="sxs-lookup"><span data-stu-id="6c961-194">True</span></span>                                             |
| <span data-ttu-id="6c961-195">É indexado</span><span class="sxs-lookup"><span data-stu-id="6c961-195">Is Indexed</span></span>             | <span data-ttu-id="6c961-196">Falso</span><span class="sxs-lookup"><span data-stu-id="6c961-196">False</span></span>                                            |
| <span data-ttu-id="6c961-197">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6c961-197">In Global Catalog</span></span>      | <span data-ttu-id="6c961-198">Falso</span><span class="sxs-lookup"><span data-stu-id="6c961-198">False</span></span>                                            |
| <span data-ttu-id="6c961-199">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6c961-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c961-200">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6c961-200">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="6c961-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c961-201">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="6c961-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c961-202">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="6c961-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c961-203">Search-Flags</span></span>           | <span data-ttu-id="6c961-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c961-204">0x00000000</span></span>                                       |
| <span data-ttu-id="6c961-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c961-205">System-Flags</span></span>           | <span data-ttu-id="6c961-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c961-206">0x00000010</span></span>                                       |
| <span data-ttu-id="6c961-207">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6c961-207">Classes used in</span></span>        | [<span data-ttu-id="6c961-208">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="6c961-208">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6c961-209">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6c961-209">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6c961-210">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c961-210">Entry</span></span> | <span data-ttu-id="6c961-211">Valor</span><span class="sxs-lookup"><span data-stu-id="6c961-211">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c961-212">ID do link</span><span class="sxs-lookup"><span data-stu-id="6c961-212">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="6c961-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c961-213">MAPI-Id</span></span>                | <span data-ttu-id="6c961-214">0x80AF</span><span class="sxs-lookup"><span data-stu-id="6c961-214">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="6c961-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c961-215">System-Only</span></span>            | <span data-ttu-id="6c961-216">Falso</span><span class="sxs-lookup"><span data-stu-id="6c961-216">False</span></span>                                                                                                 |
| <span data-ttu-id="6c961-217">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6c961-217">Is-Single-Valued</span></span>       | <span data-ttu-id="6c961-218">True</span><span class="sxs-lookup"><span data-stu-id="6c961-218">True</span></span>                                                                                                  |
| <span data-ttu-id="6c961-219">É indexado</span><span class="sxs-lookup"><span data-stu-id="6c961-219">Is Indexed</span></span>             | <span data-ttu-id="6c961-220">Falso</span><span class="sxs-lookup"><span data-stu-id="6c961-220">False</span></span>                                                                                                 |
| <span data-ttu-id="6c961-221">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6c961-221">In Global Catalog</span></span>      | <span data-ttu-id="6c961-222">Falso</span><span class="sxs-lookup"><span data-stu-id="6c961-222">False</span></span>                                                                                                 |
| <span data-ttu-id="6c961-223">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6c961-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c961-224">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6c961-224">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="6c961-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c961-225">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="6c961-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c961-226">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="6c961-227">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c961-227">Search-Flags</span></span>           | <span data-ttu-id="6c961-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c961-228">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="6c961-229">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c961-229">System-Flags</span></span>           | <span data-ttu-id="6c961-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c961-230">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="6c961-231">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6c961-231">Classes used in</span></span>        | [<span data-ttu-id="6c961-232">**Destinatário de email**</span><span class="sxs-lookup"><span data-stu-id="6c961-232">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="6c961-233">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="6c961-233">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6c961-234">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c961-234">Windows Server 2008</span></span>



| <span data-ttu-id="6c961-235">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c961-235">Entry</span></span> | <span data-ttu-id="6c961-236">Valor</span><span class="sxs-lookup"><span data-stu-id="6c961-236">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c961-237">ID do link</span><span class="sxs-lookup"><span data-stu-id="6c961-237">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="6c961-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c961-238">MAPI-Id</span></span>                | <span data-ttu-id="6c961-239">0x80AF</span><span class="sxs-lookup"><span data-stu-id="6c961-239">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="6c961-240">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c961-240">System-Only</span></span>            | <span data-ttu-id="6c961-241">Falso</span><span class="sxs-lookup"><span data-stu-id="6c961-241">False</span></span>                                                                                                 |
| <span data-ttu-id="6c961-242">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6c961-242">Is-Single-Valued</span></span>       | <span data-ttu-id="6c961-243">True</span><span class="sxs-lookup"><span data-stu-id="6c961-243">True</span></span>                                                                                                  |
| <span data-ttu-id="6c961-244">É indexado</span><span class="sxs-lookup"><span data-stu-id="6c961-244">Is Indexed</span></span>             | <span data-ttu-id="6c961-245">Falso</span><span class="sxs-lookup"><span data-stu-id="6c961-245">False</span></span>                                                                                                 |
| <span data-ttu-id="6c961-246">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6c961-246">In Global Catalog</span></span>      | <span data-ttu-id="6c961-247">Falso</span><span class="sxs-lookup"><span data-stu-id="6c961-247">False</span></span>                                                                                                 |
| <span data-ttu-id="6c961-248">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6c961-248">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c961-249">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6c961-249">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="6c961-250">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c961-250">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="6c961-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c961-251">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="6c961-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c961-252">Search-Flags</span></span>           | <span data-ttu-id="6c961-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c961-253">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="6c961-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c961-254">System-Flags</span></span>           | <span data-ttu-id="6c961-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c961-255">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="6c961-256">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6c961-256">Classes used in</span></span>        | [<span data-ttu-id="6c961-257">**Destinatário de email**</span><span class="sxs-lookup"><span data-stu-id="6c961-257">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="6c961-258">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="6c961-258">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6c961-259">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6c961-259">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6c961-260">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c961-260">Entry</span></span> | <span data-ttu-id="6c961-261">Valor</span><span class="sxs-lookup"><span data-stu-id="6c961-261">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c961-262">ID do link</span><span class="sxs-lookup"><span data-stu-id="6c961-262">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="6c961-263">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c961-263">MAPI-Id</span></span>                | <span data-ttu-id="6c961-264">0x80AF</span><span class="sxs-lookup"><span data-stu-id="6c961-264">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="6c961-265">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c961-265">System-Only</span></span>            | <span data-ttu-id="6c961-266">Falso</span><span class="sxs-lookup"><span data-stu-id="6c961-266">False</span></span>                                                                                                 |
| <span data-ttu-id="6c961-267">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6c961-267">Is-Single-Valued</span></span>       | <span data-ttu-id="6c961-268">True</span><span class="sxs-lookup"><span data-stu-id="6c961-268">True</span></span>                                                                                                  |
| <span data-ttu-id="6c961-269">É indexado</span><span class="sxs-lookup"><span data-stu-id="6c961-269">Is Indexed</span></span>             | <span data-ttu-id="6c961-270">Falso</span><span class="sxs-lookup"><span data-stu-id="6c961-270">False</span></span>                                                                                                 |
| <span data-ttu-id="6c961-271">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6c961-271">In Global Catalog</span></span>      | <span data-ttu-id="6c961-272">Falso</span><span class="sxs-lookup"><span data-stu-id="6c961-272">False</span></span>                                                                                                 |
| <span data-ttu-id="6c961-273">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6c961-273">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c961-274">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6c961-274">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="6c961-275">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c961-275">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="6c961-276">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c961-276">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="6c961-277">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c961-277">Search-Flags</span></span>           | <span data-ttu-id="6c961-278">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c961-278">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="6c961-279">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c961-279">System-Flags</span></span>           | <span data-ttu-id="6c961-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c961-280">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="6c961-281">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6c961-281">Classes used in</span></span>        | [<span data-ttu-id="6c961-282">**Destinatário de email**</span><span class="sxs-lookup"><span data-stu-id="6c961-282">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="6c961-283">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="6c961-283">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6c961-284">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6c961-284">Windows Server 2012</span></span>



| <span data-ttu-id="6c961-285">Entrada</span><span class="sxs-lookup"><span data-stu-id="6c961-285">Entry</span></span> | <span data-ttu-id="6c961-286">Valor</span><span class="sxs-lookup"><span data-stu-id="6c961-286">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c961-287">ID do link</span><span class="sxs-lookup"><span data-stu-id="6c961-287">Link-Id</span></span>                | \-                                                                                                    |
| <span data-ttu-id="6c961-288">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c961-288">MAPI-Id</span></span>                | <span data-ttu-id="6c961-289">0x80AF</span><span class="sxs-lookup"><span data-stu-id="6c961-289">0x80AF</span></span>                                                                                                |
| <span data-ttu-id="6c961-290">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c961-290">System-Only</span></span>            | <span data-ttu-id="6c961-291">Falso</span><span class="sxs-lookup"><span data-stu-id="6c961-291">False</span></span>                                                                                                 |
| <span data-ttu-id="6c961-292">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6c961-292">Is-Single-Valued</span></span>       | <span data-ttu-id="6c961-293">True</span><span class="sxs-lookup"><span data-stu-id="6c961-293">True</span></span>                                                                                                  |
| <span data-ttu-id="6c961-294">É indexado</span><span class="sxs-lookup"><span data-stu-id="6c961-294">Is Indexed</span></span>             | <span data-ttu-id="6c961-295">Falso</span><span class="sxs-lookup"><span data-stu-id="6c961-295">False</span></span>                                                                                                 |
| <span data-ttu-id="6c961-296">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6c961-296">In Global Catalog</span></span>      | <span data-ttu-id="6c961-297">Falso</span><span class="sxs-lookup"><span data-stu-id="6c961-297">False</span></span>                                                                                                 |
| <span data-ttu-id="6c961-298">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6c961-298">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c961-299">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6c961-299">O:BAG:BAD:S:</span></span>                                                                                          |
| <span data-ttu-id="6c961-300">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c961-300">Range-Lower</span></span>            | \-                                                                                                    |
| <span data-ttu-id="6c961-301">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c961-301">Range-Upper</span></span>            | \-                                                                                                    |
| <span data-ttu-id="6c961-302">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c961-302">Search-Flags</span></span>           | <span data-ttu-id="6c961-303">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c961-303">0x00000000</span></span>                                                                                            |
| <span data-ttu-id="6c961-304">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c961-304">System-Flags</span></span>           | <span data-ttu-id="6c961-305">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c961-305">0x00000010</span></span>                                                                                            |
| <span data-ttu-id="6c961-306">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6c961-306">Classes used in</span></span>        | [<span data-ttu-id="6c961-307">**Destinatário de email**</span><span class="sxs-lookup"><span data-stu-id="6c961-307">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="6c961-308">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="6c961-308">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 





