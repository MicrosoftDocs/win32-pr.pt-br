---
title: Transport-Type atributo
description: O nome distinto para um tipo de transporte que está sendo usado para conectar sites. Esse valor pode apontar para um transporte IP ou SMTP.
ms.assetid: aed18e69-3118-4cb8-b959-829106602f95
ms.tgt_platform: multiple
keywords:
- Esquema de Transport-Type do atributo AD
- Esquema de AD do atributo TransportType
topic_type:
- apiref
api_name:
- Transport-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a28c68347deb83d52b78564688a563431609fb81
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825072"
---
# <a name="transport-type-attribute"></a><span data-ttu-id="22b1f-106">Transport-Type atributo</span><span class="sxs-lookup"><span data-stu-id="22b1f-106">Transport-Type attribute</span></span>

<span data-ttu-id="22b1f-107">O nome distinto para um tipo de transporte que está sendo usado para conectar sites.</span><span class="sxs-lookup"><span data-stu-id="22b1f-107">The distinguished name for a type of transport being used to connect sites together.</span></span> <span data-ttu-id="22b1f-108">Esse valor pode apontar para um transporte IP ou SMTP.</span><span class="sxs-lookup"><span data-stu-id="22b1f-108">This value can point to an IP or SMTP transport.</span></span>



| <span data-ttu-id="22b1f-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="22b1f-109">Entry</span></span> | <span data-ttu-id="22b1f-110">Valor</span><span class="sxs-lookup"><span data-stu-id="22b1f-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="22b1f-111">CN</span><span class="sxs-lookup"><span data-stu-id="22b1f-111">CN</span></span>                | <span data-ttu-id="22b1f-112">Transport-Type</span><span class="sxs-lookup"><span data-stu-id="22b1f-112">Transport-Type</span></span>                          |
| <span data-ttu-id="22b1f-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="22b1f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="22b1f-114">transportType</span><span class="sxs-lookup"><span data-stu-id="22b1f-114">transportType</span></span>                           |
| <span data-ttu-id="22b1f-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="22b1f-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="22b1f-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="22b1f-116">Update Privilege</span></span>  | <span data-ttu-id="22b1f-117">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="22b1f-117">This value is set by the system.</span></span>        |
| <span data-ttu-id="22b1f-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="22b1f-118">Update Frequency</span></span>  | <span data-ttu-id="22b1f-119">Ao conectar sites.</span><span class="sxs-lookup"><span data-stu-id="22b1f-119">When connecting sites.</span></span>                  |
| <span data-ttu-id="22b1f-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="22b1f-120">Attribute-Id</span></span>      | <span data-ttu-id="22b1f-121">1.2.840.113556.1.4.791</span><span class="sxs-lookup"><span data-stu-id="22b1f-121">1.2.840.113556.1.4.791</span></span>                  |
| <span data-ttu-id="22b1f-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="22b1f-122">System-Id-Guid</span></span>    | <span data-ttu-id="22b1f-123">26d97374-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="22b1f-123">26d97374-6070-11d1-a9c6-0000f80367c1</span></span>    |
| <span data-ttu-id="22b1f-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="22b1f-124">Syntax</span></span>            | [<span data-ttu-id="22b1f-125">**Objeto (DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="22b1f-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="22b1f-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="22b1f-126">Implementations</span></span>

-   [<span data-ttu-id="22b1f-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="22b1f-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="22b1f-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="22b1f-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="22b1f-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="22b1f-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="22b1f-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="22b1f-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="22b1f-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="22b1f-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="22b1f-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="22b1f-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="22b1f-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="22b1f-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="22b1f-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="22b1f-134">Windows 2000 Server</span></span>



| <span data-ttu-id="22b1f-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="22b1f-135">Entry</span></span> | <span data-ttu-id="22b1f-136">Valor</span><span class="sxs-lookup"><span data-stu-id="22b1f-136">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="22b1f-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="22b1f-137">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="22b1f-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="22b1f-138">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="22b1f-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="22b1f-139">System-Only</span></span>            | <span data-ttu-id="22b1f-140">Falso</span><span class="sxs-lookup"><span data-stu-id="22b1f-140">False</span></span>                                                  |
| <span data-ttu-id="22b1f-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="22b1f-141">Is-Single-Valued</span></span>       | <span data-ttu-id="22b1f-142">True</span><span class="sxs-lookup"><span data-stu-id="22b1f-142">True</span></span>                                                   |
| <span data-ttu-id="22b1f-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="22b1f-143">Is Indexed</span></span>             | <span data-ttu-id="22b1f-144">Falso</span><span class="sxs-lookup"><span data-stu-id="22b1f-144">False</span></span>                                                  |
| <span data-ttu-id="22b1f-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="22b1f-145">In Global Catalog</span></span>      | <span data-ttu-id="22b1f-146">Falso</span><span class="sxs-lookup"><span data-stu-id="22b1f-146">False</span></span>                                                  |
| <span data-ttu-id="22b1f-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="22b1f-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="22b1f-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="22b1f-148">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="22b1f-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="22b1f-149">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="22b1f-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="22b1f-150">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="22b1f-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="22b1f-151">Search-Flags</span></span>           | <span data-ttu-id="22b1f-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="22b1f-152">0x00000000</span></span>                                             |
| <span data-ttu-id="22b1f-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="22b1f-153">System-Flags</span></span>           | <span data-ttu-id="22b1f-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="22b1f-154">0x00000010</span></span>                                             |
| <span data-ttu-id="22b1f-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="22b1f-155">Classes used in</span></span>        | [<span data-ttu-id="22b1f-156">**NTDS-conexão**</span><span class="sxs-lookup"><span data-stu-id="22b1f-156">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="22b1f-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="22b1f-157">Windows Server 2003</span></span>



| <span data-ttu-id="22b1f-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="22b1f-158">Entry</span></span> | <span data-ttu-id="22b1f-159">Valor</span><span class="sxs-lookup"><span data-stu-id="22b1f-159">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="22b1f-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="22b1f-160">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="22b1f-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="22b1f-161">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="22b1f-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="22b1f-162">System-Only</span></span>            | <span data-ttu-id="22b1f-163">Falso</span><span class="sxs-lookup"><span data-stu-id="22b1f-163">False</span></span>                                                  |
| <span data-ttu-id="22b1f-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="22b1f-164">Is-Single-Valued</span></span>       | <span data-ttu-id="22b1f-165">True</span><span class="sxs-lookup"><span data-stu-id="22b1f-165">True</span></span>                                                   |
| <span data-ttu-id="22b1f-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="22b1f-166">Is Indexed</span></span>             | <span data-ttu-id="22b1f-167">Falso</span><span class="sxs-lookup"><span data-stu-id="22b1f-167">False</span></span>                                                  |
| <span data-ttu-id="22b1f-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="22b1f-168">In Global Catalog</span></span>      | <span data-ttu-id="22b1f-169">Falso</span><span class="sxs-lookup"><span data-stu-id="22b1f-169">False</span></span>                                                  |
| <span data-ttu-id="22b1f-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="22b1f-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="22b1f-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="22b1f-171">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="22b1f-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="22b1f-172">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="22b1f-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="22b1f-173">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="22b1f-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="22b1f-174">Search-Flags</span></span>           | <span data-ttu-id="22b1f-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="22b1f-175">0x00000000</span></span>                                             |
| <span data-ttu-id="22b1f-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="22b1f-176">System-Flags</span></span>           | <span data-ttu-id="22b1f-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="22b1f-177">0x00000010</span></span>                                             |
| <span data-ttu-id="22b1f-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="22b1f-178">Classes used in</span></span>        | [<span data-ttu-id="22b1f-179">**NTDS-conexão**</span><span class="sxs-lookup"><span data-stu-id="22b1f-179">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="adam"></a><span data-ttu-id="22b1f-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="22b1f-180">ADAM</span></span>



| <span data-ttu-id="22b1f-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="22b1f-181">Entry</span></span> | <span data-ttu-id="22b1f-182">Valor</span><span class="sxs-lookup"><span data-stu-id="22b1f-182">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="22b1f-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="22b1f-183">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="22b1f-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="22b1f-184">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="22b1f-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="22b1f-185">System-Only</span></span>            | <span data-ttu-id="22b1f-186">Falso</span><span class="sxs-lookup"><span data-stu-id="22b1f-186">False</span></span>                                                  |
| <span data-ttu-id="22b1f-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="22b1f-187">Is-Single-Valued</span></span>       | <span data-ttu-id="22b1f-188">True</span><span class="sxs-lookup"><span data-stu-id="22b1f-188">True</span></span>                                                   |
| <span data-ttu-id="22b1f-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="22b1f-189">Is Indexed</span></span>             | <span data-ttu-id="22b1f-190">Falso</span><span class="sxs-lookup"><span data-stu-id="22b1f-190">False</span></span>                                                  |
| <span data-ttu-id="22b1f-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="22b1f-191">In Global Catalog</span></span>      | <span data-ttu-id="22b1f-192">Falso</span><span class="sxs-lookup"><span data-stu-id="22b1f-192">False</span></span>                                                  |
| <span data-ttu-id="22b1f-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="22b1f-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="22b1f-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="22b1f-194">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="22b1f-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="22b1f-195">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="22b1f-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="22b1f-196">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="22b1f-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="22b1f-197">Search-Flags</span></span>           | <span data-ttu-id="22b1f-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="22b1f-198">0x00000000</span></span>                                             |
| <span data-ttu-id="22b1f-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="22b1f-199">System-Flags</span></span>           | <span data-ttu-id="22b1f-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="22b1f-200">0x00000010</span></span>                                             |
| <span data-ttu-id="22b1f-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="22b1f-201">Classes used in</span></span>        | [<span data-ttu-id="22b1f-202">**NTDS-conexão**</span><span class="sxs-lookup"><span data-stu-id="22b1f-202">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="22b1f-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="22b1f-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="22b1f-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="22b1f-204">Entry</span></span> | <span data-ttu-id="22b1f-205">Valor</span><span class="sxs-lookup"><span data-stu-id="22b1f-205">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="22b1f-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="22b1f-206">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="22b1f-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="22b1f-207">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="22b1f-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="22b1f-208">System-Only</span></span>            | <span data-ttu-id="22b1f-209">Falso</span><span class="sxs-lookup"><span data-stu-id="22b1f-209">False</span></span>                                                  |
| <span data-ttu-id="22b1f-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="22b1f-210">Is-Single-Valued</span></span>       | <span data-ttu-id="22b1f-211">True</span><span class="sxs-lookup"><span data-stu-id="22b1f-211">True</span></span>                                                   |
| <span data-ttu-id="22b1f-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="22b1f-212">Is Indexed</span></span>             | <span data-ttu-id="22b1f-213">Falso</span><span class="sxs-lookup"><span data-stu-id="22b1f-213">False</span></span>                                                  |
| <span data-ttu-id="22b1f-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="22b1f-214">In Global Catalog</span></span>      | <span data-ttu-id="22b1f-215">Falso</span><span class="sxs-lookup"><span data-stu-id="22b1f-215">False</span></span>                                                  |
| <span data-ttu-id="22b1f-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="22b1f-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="22b1f-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="22b1f-217">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="22b1f-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="22b1f-218">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="22b1f-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="22b1f-219">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="22b1f-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="22b1f-220">Search-Flags</span></span>           | <span data-ttu-id="22b1f-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="22b1f-221">0x00000000</span></span>                                             |
| <span data-ttu-id="22b1f-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="22b1f-222">System-Flags</span></span>           | <span data-ttu-id="22b1f-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="22b1f-223">0x00000010</span></span>                                             |
| <span data-ttu-id="22b1f-224">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="22b1f-224">Classes used in</span></span>        | [<span data-ttu-id="22b1f-225">**NTDS-conexão**</span><span class="sxs-lookup"><span data-stu-id="22b1f-225">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="22b1f-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="22b1f-226">Windows Server 2008</span></span>



| <span data-ttu-id="22b1f-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="22b1f-227">Entry</span></span> | <span data-ttu-id="22b1f-228">Valor</span><span class="sxs-lookup"><span data-stu-id="22b1f-228">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="22b1f-229">ID do link</span><span class="sxs-lookup"><span data-stu-id="22b1f-229">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="22b1f-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="22b1f-230">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="22b1f-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="22b1f-231">System-Only</span></span>            | <span data-ttu-id="22b1f-232">Falso</span><span class="sxs-lookup"><span data-stu-id="22b1f-232">False</span></span>                                                  |
| <span data-ttu-id="22b1f-233">É de valor único</span><span class="sxs-lookup"><span data-stu-id="22b1f-233">Is-Single-Valued</span></span>       | <span data-ttu-id="22b1f-234">True</span><span class="sxs-lookup"><span data-stu-id="22b1f-234">True</span></span>                                                   |
| <span data-ttu-id="22b1f-235">É indexado</span><span class="sxs-lookup"><span data-stu-id="22b1f-235">Is Indexed</span></span>             | <span data-ttu-id="22b1f-236">Falso</span><span class="sxs-lookup"><span data-stu-id="22b1f-236">False</span></span>                                                  |
| <span data-ttu-id="22b1f-237">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="22b1f-237">In Global Catalog</span></span>      | <span data-ttu-id="22b1f-238">Falso</span><span class="sxs-lookup"><span data-stu-id="22b1f-238">False</span></span>                                                  |
| <span data-ttu-id="22b1f-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="22b1f-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="22b1f-240">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="22b1f-240">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="22b1f-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="22b1f-241">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="22b1f-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="22b1f-242">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="22b1f-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="22b1f-243">Search-Flags</span></span>           | <span data-ttu-id="22b1f-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="22b1f-244">0x00000000</span></span>                                             |
| <span data-ttu-id="22b1f-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="22b1f-245">System-Flags</span></span>           | <span data-ttu-id="22b1f-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="22b1f-246">0x00000010</span></span>                                             |
| <span data-ttu-id="22b1f-247">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="22b1f-247">Classes used in</span></span>        | [<span data-ttu-id="22b1f-248">**NTDS-conexão**</span><span class="sxs-lookup"><span data-stu-id="22b1f-248">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="22b1f-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="22b1f-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="22b1f-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="22b1f-250">Entry</span></span> | <span data-ttu-id="22b1f-251">Valor</span><span class="sxs-lookup"><span data-stu-id="22b1f-251">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="22b1f-252">ID do link</span><span class="sxs-lookup"><span data-stu-id="22b1f-252">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="22b1f-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="22b1f-253">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="22b1f-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="22b1f-254">System-Only</span></span>            | <span data-ttu-id="22b1f-255">Falso</span><span class="sxs-lookup"><span data-stu-id="22b1f-255">False</span></span>                                                  |
| <span data-ttu-id="22b1f-256">É de valor único</span><span class="sxs-lookup"><span data-stu-id="22b1f-256">Is-Single-Valued</span></span>       | <span data-ttu-id="22b1f-257">True</span><span class="sxs-lookup"><span data-stu-id="22b1f-257">True</span></span>                                                   |
| <span data-ttu-id="22b1f-258">É indexado</span><span class="sxs-lookup"><span data-stu-id="22b1f-258">Is Indexed</span></span>             | <span data-ttu-id="22b1f-259">Falso</span><span class="sxs-lookup"><span data-stu-id="22b1f-259">False</span></span>                                                  |
| <span data-ttu-id="22b1f-260">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="22b1f-260">In Global Catalog</span></span>      | <span data-ttu-id="22b1f-261">Falso</span><span class="sxs-lookup"><span data-stu-id="22b1f-261">False</span></span>                                                  |
| <span data-ttu-id="22b1f-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="22b1f-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="22b1f-263">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="22b1f-263">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="22b1f-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="22b1f-264">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="22b1f-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="22b1f-265">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="22b1f-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="22b1f-266">Search-Flags</span></span>           | <span data-ttu-id="22b1f-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="22b1f-267">0x00000000</span></span>                                             |
| <span data-ttu-id="22b1f-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="22b1f-268">System-Flags</span></span>           | <span data-ttu-id="22b1f-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="22b1f-269">0x00000010</span></span>                                             |
| <span data-ttu-id="22b1f-270">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="22b1f-270">Classes used in</span></span>        | [<span data-ttu-id="22b1f-271">**NTDS-conexão**</span><span class="sxs-lookup"><span data-stu-id="22b1f-271">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="22b1f-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="22b1f-272">Windows Server 2012</span></span>



| <span data-ttu-id="22b1f-273">Entrada</span><span class="sxs-lookup"><span data-stu-id="22b1f-273">Entry</span></span> | <span data-ttu-id="22b1f-274">Valor</span><span class="sxs-lookup"><span data-stu-id="22b1f-274">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="22b1f-275">ID do link</span><span class="sxs-lookup"><span data-stu-id="22b1f-275">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="22b1f-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="22b1f-276">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="22b1f-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="22b1f-277">System-Only</span></span>            | <span data-ttu-id="22b1f-278">Falso</span><span class="sxs-lookup"><span data-stu-id="22b1f-278">False</span></span>                                                  |
| <span data-ttu-id="22b1f-279">É de valor único</span><span class="sxs-lookup"><span data-stu-id="22b1f-279">Is-Single-Valued</span></span>       | <span data-ttu-id="22b1f-280">True</span><span class="sxs-lookup"><span data-stu-id="22b1f-280">True</span></span>                                                   |
| <span data-ttu-id="22b1f-281">É indexado</span><span class="sxs-lookup"><span data-stu-id="22b1f-281">Is Indexed</span></span>             | <span data-ttu-id="22b1f-282">Falso</span><span class="sxs-lookup"><span data-stu-id="22b1f-282">False</span></span>                                                  |
| <span data-ttu-id="22b1f-283">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="22b1f-283">In Global Catalog</span></span>      | <span data-ttu-id="22b1f-284">Falso</span><span class="sxs-lookup"><span data-stu-id="22b1f-284">False</span></span>                                                  |
| <span data-ttu-id="22b1f-285">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="22b1f-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="22b1f-286">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="22b1f-286">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="22b1f-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="22b1f-287">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="22b1f-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="22b1f-288">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="22b1f-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="22b1f-289">Search-Flags</span></span>           | <span data-ttu-id="22b1f-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="22b1f-290">0x00000000</span></span>                                             |
| <span data-ttu-id="22b1f-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="22b1f-291">System-Flags</span></span>           | <span data-ttu-id="22b1f-292">0x00000010</span><span class="sxs-lookup"><span data-stu-id="22b1f-292">0x00000010</span></span>                                             |
| <span data-ttu-id="22b1f-293">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="22b1f-293">Classes used in</span></span>        | [<span data-ttu-id="22b1f-294">**NTDS-conexão**</span><span class="sxs-lookup"><span data-stu-id="22b1f-294">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



 

 





