---
title: DNS-Property atributo
description: Usado para armazenar configurações binárias (Propriedades) em objetos de zona DNS.
ms.assetid: 55ea38cd-6b5b-4500-8e68-ae4d35e4b177
ms.tgt_platform: multiple
keywords:
- Esquema de DNS-Property do atributo AD
- Esquema de AD do atributo dNSProperty
topic_type:
- apiref
api_name:
- DNS-Property
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f8fd18f4524ec0bf61a609d21a361668ed295b6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105756488"
---
# <a name="dns-property-attribute"></a><span data-ttu-id="e465c-105">DNS-Property atributo</span><span class="sxs-lookup"><span data-stu-id="e465c-105">DNS-Property attribute</span></span>

<span data-ttu-id="e465c-106">Usado para armazenar configurações binárias (Propriedades) em objetos de zona DNS.</span><span class="sxs-lookup"><span data-stu-id="e465c-106">Used to store binary settings (properties) on DNS zone objects.</span></span>



| <span data-ttu-id="e465c-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="e465c-107">Entry</span></span> | <span data-ttu-id="e465c-108">Valor</span><span class="sxs-lookup"><span data-stu-id="e465c-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="e465c-109">CN</span><span class="sxs-lookup"><span data-stu-id="e465c-109">CN</span></span>                | <span data-ttu-id="e465c-110">DNS-Property</span><span class="sxs-lookup"><span data-stu-id="e465c-110">DNS-Property</span></span>                                          |
| <span data-ttu-id="e465c-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e465c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e465c-112">dNSProperty</span><span class="sxs-lookup"><span data-stu-id="e465c-112">dNSProperty</span></span>                                           |
| <span data-ttu-id="e465c-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="e465c-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="e465c-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="e465c-114">Update Privilege</span></span>  | <span data-ttu-id="e465c-115">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="e465c-115">This value is set by the system.</span></span>                      |
| <span data-ttu-id="e465c-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="e465c-116">Update Frequency</span></span>  | <span data-ttu-id="e465c-117">Sempre que os registros de zona DNS são alterados.</span><span class="sxs-lookup"><span data-stu-id="e465c-117">Whenever DNS zone records change.</span></span>                     |
| <span data-ttu-id="e465c-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e465c-118">Attribute-Id</span></span>      | <span data-ttu-id="e465c-119">1.2.840.113556.1.4.1306</span><span class="sxs-lookup"><span data-stu-id="e465c-119">1.2.840.113556.1.4.1306</span></span>                               |
| <span data-ttu-id="e465c-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e465c-120">System-Id-Guid</span></span>    | <span data-ttu-id="e465c-121">675a15fe-3b70-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="e465c-121">675a15fe-3b70-11d2-90cc-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="e465c-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="e465c-122">Syntax</span></span>            | [<span data-ttu-id="e465c-123">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="e465c-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="e465c-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="e465c-124">Implementations</span></span>

-   [<span data-ttu-id="e465c-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e465c-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e465c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e465c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e465c-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e465c-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e465c-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e465c-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e465c-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e465c-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e465c-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e465c-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e465c-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e465c-131">Windows 2000 Server</span></span>



| <span data-ttu-id="e465c-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="e465c-132">Entry</span></span> | <span data-ttu-id="e465c-133">Valor</span><span class="sxs-lookup"><span data-stu-id="e465c-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e465c-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="e465c-134">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="e465c-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e465c-135">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="e465c-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="e465c-136">System-Only</span></span>            | <span data-ttu-id="e465c-137">Falso</span><span class="sxs-lookup"><span data-stu-id="e465c-137">False</span></span>                                                                             |
| <span data-ttu-id="e465c-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e465c-138">Is-Single-Valued</span></span>       | <span data-ttu-id="e465c-139">Falso</span><span class="sxs-lookup"><span data-stu-id="e465c-139">False</span></span>                                                                             |
| <span data-ttu-id="e465c-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="e465c-140">Is Indexed</span></span>             | <span data-ttu-id="e465c-141">Falso</span><span class="sxs-lookup"><span data-stu-id="e465c-141">False</span></span>                                                                             |
| <span data-ttu-id="e465c-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e465c-142">In Global Catalog</span></span>      | <span data-ttu-id="e465c-143">Falso</span><span class="sxs-lookup"><span data-stu-id="e465c-143">False</span></span>                                                                             |
| <span data-ttu-id="e465c-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e465c-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="e465c-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e465c-145">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="e465c-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e465c-146">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="e465c-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e465c-147">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="e465c-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e465c-148">Search-Flags</span></span>           | <span data-ttu-id="e465c-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e465c-149">0x00000000</span></span>                                                                        |
| <span data-ttu-id="e465c-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e465c-150">System-Flags</span></span>           | <span data-ttu-id="e465c-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e465c-151">0x00000010</span></span>                                                                        |
| <span data-ttu-id="e465c-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e465c-152">Classes used in</span></span>        | [<span data-ttu-id="e465c-153">**Nó DNS**</span><span class="sxs-lookup"><span data-stu-id="e465c-153">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="e465c-154">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="e465c-154">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e465c-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e465c-155">Windows Server 2003</span></span>



| <span data-ttu-id="e465c-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="e465c-156">Entry</span></span> | <span data-ttu-id="e465c-157">Valor</span><span class="sxs-lookup"><span data-stu-id="e465c-157">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e465c-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="e465c-158">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="e465c-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e465c-159">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="e465c-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="e465c-160">System-Only</span></span>            | <span data-ttu-id="e465c-161">Falso</span><span class="sxs-lookup"><span data-stu-id="e465c-161">False</span></span>                                                                             |
| <span data-ttu-id="e465c-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e465c-162">Is-Single-Valued</span></span>       | <span data-ttu-id="e465c-163">Falso</span><span class="sxs-lookup"><span data-stu-id="e465c-163">False</span></span>                                                                             |
| <span data-ttu-id="e465c-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="e465c-164">Is Indexed</span></span>             | <span data-ttu-id="e465c-165">Falso</span><span class="sxs-lookup"><span data-stu-id="e465c-165">False</span></span>                                                                             |
| <span data-ttu-id="e465c-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e465c-166">In Global Catalog</span></span>      | <span data-ttu-id="e465c-167">Falso</span><span class="sxs-lookup"><span data-stu-id="e465c-167">False</span></span>                                                                             |
| <span data-ttu-id="e465c-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e465c-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="e465c-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e465c-169">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="e465c-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e465c-170">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="e465c-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e465c-171">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="e465c-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e465c-172">Search-Flags</span></span>           | <span data-ttu-id="e465c-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e465c-173">0x00000000</span></span>                                                                        |
| <span data-ttu-id="e465c-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e465c-174">System-Flags</span></span>           | <span data-ttu-id="e465c-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e465c-175">0x00000010</span></span>                                                                        |
| <span data-ttu-id="e465c-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e465c-176">Classes used in</span></span>        | [<span data-ttu-id="e465c-177">**Nó DNS**</span><span class="sxs-lookup"><span data-stu-id="e465c-177">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="e465c-178">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="e465c-178">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e465c-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e465c-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e465c-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="e465c-180">Entry</span></span> | <span data-ttu-id="e465c-181">Valor</span><span class="sxs-lookup"><span data-stu-id="e465c-181">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e465c-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="e465c-182">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="e465c-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e465c-183">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="e465c-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="e465c-184">System-Only</span></span>            | <span data-ttu-id="e465c-185">Falso</span><span class="sxs-lookup"><span data-stu-id="e465c-185">False</span></span>                                                                             |
| <span data-ttu-id="e465c-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e465c-186">Is-Single-Valued</span></span>       | <span data-ttu-id="e465c-187">Falso</span><span class="sxs-lookup"><span data-stu-id="e465c-187">False</span></span>                                                                             |
| <span data-ttu-id="e465c-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="e465c-188">Is Indexed</span></span>             | <span data-ttu-id="e465c-189">Falso</span><span class="sxs-lookup"><span data-stu-id="e465c-189">False</span></span>                                                                             |
| <span data-ttu-id="e465c-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e465c-190">In Global Catalog</span></span>      | <span data-ttu-id="e465c-191">Falso</span><span class="sxs-lookup"><span data-stu-id="e465c-191">False</span></span>                                                                             |
| <span data-ttu-id="e465c-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e465c-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="e465c-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e465c-193">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="e465c-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e465c-194">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="e465c-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e465c-195">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="e465c-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e465c-196">Search-Flags</span></span>           | <span data-ttu-id="e465c-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e465c-197">0x00000000</span></span>                                                                        |
| <span data-ttu-id="e465c-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e465c-198">System-Flags</span></span>           | <span data-ttu-id="e465c-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e465c-199">0x00000010</span></span>                                                                        |
| <span data-ttu-id="e465c-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e465c-200">Classes used in</span></span>        | [<span data-ttu-id="e465c-201">**Nó DNS**</span><span class="sxs-lookup"><span data-stu-id="e465c-201">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="e465c-202">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="e465c-202">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e465c-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e465c-203">Windows Server 2008</span></span>



| <span data-ttu-id="e465c-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="e465c-204">Entry</span></span> | <span data-ttu-id="e465c-205">Valor</span><span class="sxs-lookup"><span data-stu-id="e465c-205">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e465c-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="e465c-206">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="e465c-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e465c-207">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="e465c-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="e465c-208">System-Only</span></span>            | <span data-ttu-id="e465c-209">Falso</span><span class="sxs-lookup"><span data-stu-id="e465c-209">False</span></span>                                                                             |
| <span data-ttu-id="e465c-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e465c-210">Is-Single-Valued</span></span>       | <span data-ttu-id="e465c-211">Falso</span><span class="sxs-lookup"><span data-stu-id="e465c-211">False</span></span>                                                                             |
| <span data-ttu-id="e465c-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="e465c-212">Is Indexed</span></span>             | <span data-ttu-id="e465c-213">Falso</span><span class="sxs-lookup"><span data-stu-id="e465c-213">False</span></span>                                                                             |
| <span data-ttu-id="e465c-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e465c-214">In Global Catalog</span></span>      | <span data-ttu-id="e465c-215">Falso</span><span class="sxs-lookup"><span data-stu-id="e465c-215">False</span></span>                                                                             |
| <span data-ttu-id="e465c-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e465c-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="e465c-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e465c-217">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="e465c-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e465c-218">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="e465c-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e465c-219">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="e465c-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e465c-220">Search-Flags</span></span>           | <span data-ttu-id="e465c-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e465c-221">0x00000000</span></span>                                                                        |
| <span data-ttu-id="e465c-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e465c-222">System-Flags</span></span>           | <span data-ttu-id="e465c-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e465c-223">0x00000010</span></span>                                                                        |
| <span data-ttu-id="e465c-224">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e465c-224">Classes used in</span></span>        | [<span data-ttu-id="e465c-225">**Nó DNS**</span><span class="sxs-lookup"><span data-stu-id="e465c-225">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="e465c-226">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="e465c-226">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e465c-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e465c-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e465c-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="e465c-228">Entry</span></span> | <span data-ttu-id="e465c-229">Valor</span><span class="sxs-lookup"><span data-stu-id="e465c-229">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e465c-230">ID do link</span><span class="sxs-lookup"><span data-stu-id="e465c-230">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="e465c-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e465c-231">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="e465c-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="e465c-232">System-Only</span></span>            | <span data-ttu-id="e465c-233">Falso</span><span class="sxs-lookup"><span data-stu-id="e465c-233">False</span></span>                                                                             |
| <span data-ttu-id="e465c-234">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e465c-234">Is-Single-Valued</span></span>       | <span data-ttu-id="e465c-235">Falso</span><span class="sxs-lookup"><span data-stu-id="e465c-235">False</span></span>                                                                             |
| <span data-ttu-id="e465c-236">É indexado</span><span class="sxs-lookup"><span data-stu-id="e465c-236">Is Indexed</span></span>             | <span data-ttu-id="e465c-237">Falso</span><span class="sxs-lookup"><span data-stu-id="e465c-237">False</span></span>                                                                             |
| <span data-ttu-id="e465c-238">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e465c-238">In Global Catalog</span></span>      | <span data-ttu-id="e465c-239">Falso</span><span class="sxs-lookup"><span data-stu-id="e465c-239">False</span></span>                                                                             |
| <span data-ttu-id="e465c-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e465c-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="e465c-241">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e465c-241">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="e465c-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e465c-242">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="e465c-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e465c-243">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="e465c-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e465c-244">Search-Flags</span></span>           | <span data-ttu-id="e465c-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e465c-245">0x00000000</span></span>                                                                        |
| <span data-ttu-id="e465c-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e465c-246">System-Flags</span></span>           | <span data-ttu-id="e465c-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e465c-247">0x00000010</span></span>                                                                        |
| <span data-ttu-id="e465c-248">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e465c-248">Classes used in</span></span>        | [<span data-ttu-id="e465c-249">**Nó DNS**</span><span class="sxs-lookup"><span data-stu-id="e465c-249">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="e465c-250">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="e465c-250">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e465c-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e465c-251">Windows Server 2012</span></span>



| <span data-ttu-id="e465c-252">Entrada</span><span class="sxs-lookup"><span data-stu-id="e465c-252">Entry</span></span> | <span data-ttu-id="e465c-253">Valor</span><span class="sxs-lookup"><span data-stu-id="e465c-253">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e465c-254">ID do link</span><span class="sxs-lookup"><span data-stu-id="e465c-254">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="e465c-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e465c-255">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="e465c-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="e465c-256">System-Only</span></span>            | <span data-ttu-id="e465c-257">Falso</span><span class="sxs-lookup"><span data-stu-id="e465c-257">False</span></span>                                                                             |
| <span data-ttu-id="e465c-258">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e465c-258">Is-Single-Valued</span></span>       | <span data-ttu-id="e465c-259">Falso</span><span class="sxs-lookup"><span data-stu-id="e465c-259">False</span></span>                                                                             |
| <span data-ttu-id="e465c-260">É indexado</span><span class="sxs-lookup"><span data-stu-id="e465c-260">Is Indexed</span></span>             | <span data-ttu-id="e465c-261">Falso</span><span class="sxs-lookup"><span data-stu-id="e465c-261">False</span></span>                                                                             |
| <span data-ttu-id="e465c-262">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e465c-262">In Global Catalog</span></span>      | <span data-ttu-id="e465c-263">Falso</span><span class="sxs-lookup"><span data-stu-id="e465c-263">False</span></span>                                                                             |
| <span data-ttu-id="e465c-264">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e465c-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="e465c-265">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e465c-265">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="e465c-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e465c-266">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="e465c-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e465c-267">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="e465c-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e465c-268">Search-Flags</span></span>           | <span data-ttu-id="e465c-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e465c-269">0x00000000</span></span>                                                                        |
| <span data-ttu-id="e465c-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e465c-270">System-Flags</span></span>           | <span data-ttu-id="e465c-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e465c-271">0x00000010</span></span>                                                                        |
| <span data-ttu-id="e465c-272">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e465c-272">Classes used in</span></span>        | [<span data-ttu-id="e465c-273">**Nó DNS**</span><span class="sxs-lookup"><span data-stu-id="e465c-273">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="e465c-274">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="e465c-274">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



 

 





