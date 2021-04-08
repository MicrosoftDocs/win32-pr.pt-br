---
title: Dns-Record atributo
description: Usado para armazenar registros de recursos DNS binários em objetos DNS.
ms.assetid: 2d5a17da-0efc-450e-b247-3ab6d2de3a5d
ms.tgt_platform: multiple
keywords:
- Esquema de Dns-Record do atributo AD
- Esquema de AD do atributo dnsRecord
topic_type:
- apiref
api_name:
- Dns-Record
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 013fa5ef4a9fcec151f996c347cdfd525438aa7d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104087122"
---
# <a name="dns-record-attribute"></a><span data-ttu-id="f3b0e-105">Dns-Record atributo</span><span class="sxs-lookup"><span data-stu-id="f3b0e-105">Dns-Record attribute</span></span>

<span data-ttu-id="f3b0e-106">Usado para armazenar registros de recursos DNS binários em objetos DNS.</span><span class="sxs-lookup"><span data-stu-id="f3b0e-106">Used to store binary DNS resource records on DNS objects.</span></span>



| <span data-ttu-id="f3b0e-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="f3b0e-107">Entry</span></span> | <span data-ttu-id="f3b0e-108">Valor</span><span class="sxs-lookup"><span data-stu-id="f3b0e-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="f3b0e-109">CN</span><span class="sxs-lookup"><span data-stu-id="f3b0e-109">CN</span></span>                | <span data-ttu-id="f3b0e-110">Dns-Record</span><span class="sxs-lookup"><span data-stu-id="f3b0e-110">Dns-Record</span></span>                                            |
| <span data-ttu-id="f3b0e-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f3b0e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f3b0e-112">dnsRecord</span><span class="sxs-lookup"><span data-stu-id="f3b0e-112">dnsRecord</span></span>                                             |
| <span data-ttu-id="f3b0e-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="f3b0e-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="f3b0e-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="f3b0e-114">Update Privilege</span></span>  | <span data-ttu-id="f3b0e-115">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="f3b0e-115">This value is set by the system.</span></span>                      |
| <span data-ttu-id="f3b0e-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="f3b0e-116">Update Frequency</span></span>  | <span data-ttu-id="f3b0e-117">Sempre que os registros de recurso DNS forem alterados.</span><span class="sxs-lookup"><span data-stu-id="f3b0e-117">Whenever DNS resource records change.</span></span>                 |
| <span data-ttu-id="f3b0e-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f3b0e-118">Attribute-Id</span></span>      | <span data-ttu-id="f3b0e-119">1.2.840.113556.1.4.382</span><span class="sxs-lookup"><span data-stu-id="f3b0e-119">1.2.840.113556.1.4.382</span></span>                                |
| <span data-ttu-id="f3b0e-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f3b0e-120">System-Id-Guid</span></span>    | <span data-ttu-id="f3b0e-121">e0fa1e69-9b45-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="f3b0e-121">e0fa1e69-9b45-11d0-afdd-00c04fd930c9</span></span>                  |
| <span data-ttu-id="f3b0e-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3b0e-122">Syntax</span></span>            | [<span data-ttu-id="f3b0e-123">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="f3b0e-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="f3b0e-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="f3b0e-124">Implementations</span></span>

-   [<span data-ttu-id="f3b0e-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f3b0e-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f3b0e-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f3b0e-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f3b0e-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f3b0e-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f3b0e-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f3b0e-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f3b0e-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f3b0e-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f3b0e-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f3b0e-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f3b0e-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f3b0e-131">Windows 2000 Server</span></span>



| <span data-ttu-id="f3b0e-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="f3b0e-132">Entry</span></span> | <span data-ttu-id="f3b0e-133">Valor</span><span class="sxs-lookup"><span data-stu-id="f3b0e-133">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f3b0e-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="f3b0e-134">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="f3b0e-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3b0e-135">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="f3b0e-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3b0e-136">System-Only</span></span>            | <span data-ttu-id="f3b0e-137">Falso</span><span class="sxs-lookup"><span data-stu-id="f3b0e-137">False</span></span>                                    |
| <span data-ttu-id="f3b0e-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f3b0e-138">Is-Single-Valued</span></span>       | <span data-ttu-id="f3b0e-139">Falso</span><span class="sxs-lookup"><span data-stu-id="f3b0e-139">False</span></span>                                    |
| <span data-ttu-id="f3b0e-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="f3b0e-140">Is Indexed</span></span>             | <span data-ttu-id="f3b0e-141">Falso</span><span class="sxs-lookup"><span data-stu-id="f3b0e-141">False</span></span>                                    |
| <span data-ttu-id="f3b0e-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f3b0e-142">In Global Catalog</span></span>      | <span data-ttu-id="f3b0e-143">Falso</span><span class="sxs-lookup"><span data-stu-id="f3b0e-143">False</span></span>                                    |
| <span data-ttu-id="f3b0e-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f3b0e-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3b0e-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f3b0e-145">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f3b0e-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3b0e-146">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f3b0e-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3b0e-147">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f3b0e-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3b0e-148">Search-Flags</span></span>           | <span data-ttu-id="f3b0e-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3b0e-149">0x00000000</span></span>                               |
| <span data-ttu-id="f3b0e-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3b0e-150">System-Flags</span></span>           | <span data-ttu-id="f3b0e-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f3b0e-151">0x00000010</span></span>                               |
| <span data-ttu-id="f3b0e-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f3b0e-152">Classes used in</span></span>        | [<span data-ttu-id="f3b0e-153">**Nó DNS**</span><span class="sxs-lookup"><span data-stu-id="f3b0e-153">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f3b0e-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f3b0e-154">Windows Server 2003</span></span>



| <span data-ttu-id="f3b0e-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="f3b0e-155">Entry</span></span> | <span data-ttu-id="f3b0e-156">Valor</span><span class="sxs-lookup"><span data-stu-id="f3b0e-156">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f3b0e-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="f3b0e-157">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="f3b0e-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3b0e-158">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="f3b0e-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3b0e-159">System-Only</span></span>            | <span data-ttu-id="f3b0e-160">Falso</span><span class="sxs-lookup"><span data-stu-id="f3b0e-160">False</span></span>                                    |
| <span data-ttu-id="f3b0e-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f3b0e-161">Is-Single-Valued</span></span>       | <span data-ttu-id="f3b0e-162">Falso</span><span class="sxs-lookup"><span data-stu-id="f3b0e-162">False</span></span>                                    |
| <span data-ttu-id="f3b0e-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="f3b0e-163">Is Indexed</span></span>             | <span data-ttu-id="f3b0e-164">Falso</span><span class="sxs-lookup"><span data-stu-id="f3b0e-164">False</span></span>                                    |
| <span data-ttu-id="f3b0e-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f3b0e-165">In Global Catalog</span></span>      | <span data-ttu-id="f3b0e-166">Falso</span><span class="sxs-lookup"><span data-stu-id="f3b0e-166">False</span></span>                                    |
| <span data-ttu-id="f3b0e-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f3b0e-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3b0e-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f3b0e-168">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f3b0e-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3b0e-169">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f3b0e-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3b0e-170">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f3b0e-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3b0e-171">Search-Flags</span></span>           | <span data-ttu-id="f3b0e-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3b0e-172">0x00000000</span></span>                               |
| <span data-ttu-id="f3b0e-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3b0e-173">System-Flags</span></span>           | <span data-ttu-id="f3b0e-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f3b0e-174">0x00000010</span></span>                               |
| <span data-ttu-id="f3b0e-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f3b0e-175">Classes used in</span></span>        | [<span data-ttu-id="f3b0e-176">**Nó DNS**</span><span class="sxs-lookup"><span data-stu-id="f3b0e-176">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f3b0e-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f3b0e-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f3b0e-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="f3b0e-178">Entry</span></span> | <span data-ttu-id="f3b0e-179">Valor</span><span class="sxs-lookup"><span data-stu-id="f3b0e-179">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f3b0e-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="f3b0e-180">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="f3b0e-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3b0e-181">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="f3b0e-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3b0e-182">System-Only</span></span>            | <span data-ttu-id="f3b0e-183">Falso</span><span class="sxs-lookup"><span data-stu-id="f3b0e-183">False</span></span>                                    |
| <span data-ttu-id="f3b0e-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f3b0e-184">Is-Single-Valued</span></span>       | <span data-ttu-id="f3b0e-185">Falso</span><span class="sxs-lookup"><span data-stu-id="f3b0e-185">False</span></span>                                    |
| <span data-ttu-id="f3b0e-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="f3b0e-186">Is Indexed</span></span>             | <span data-ttu-id="f3b0e-187">Falso</span><span class="sxs-lookup"><span data-stu-id="f3b0e-187">False</span></span>                                    |
| <span data-ttu-id="f3b0e-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f3b0e-188">In Global Catalog</span></span>      | <span data-ttu-id="f3b0e-189">Falso</span><span class="sxs-lookup"><span data-stu-id="f3b0e-189">False</span></span>                                    |
| <span data-ttu-id="f3b0e-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f3b0e-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3b0e-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f3b0e-191">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f3b0e-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3b0e-192">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f3b0e-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3b0e-193">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f3b0e-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3b0e-194">Search-Flags</span></span>           | <span data-ttu-id="f3b0e-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3b0e-195">0x00000000</span></span>                               |
| <span data-ttu-id="f3b0e-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3b0e-196">System-Flags</span></span>           | <span data-ttu-id="f3b0e-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f3b0e-197">0x00000010</span></span>                               |
| <span data-ttu-id="f3b0e-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f3b0e-198">Classes used in</span></span>        | [<span data-ttu-id="f3b0e-199">**Nó DNS**</span><span class="sxs-lookup"><span data-stu-id="f3b0e-199">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f3b0e-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3b0e-200">Windows Server 2008</span></span>



| <span data-ttu-id="f3b0e-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="f3b0e-201">Entry</span></span> | <span data-ttu-id="f3b0e-202">Valor</span><span class="sxs-lookup"><span data-stu-id="f3b0e-202">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f3b0e-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="f3b0e-203">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="f3b0e-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3b0e-204">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="f3b0e-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3b0e-205">System-Only</span></span>            | <span data-ttu-id="f3b0e-206">Falso</span><span class="sxs-lookup"><span data-stu-id="f3b0e-206">False</span></span>                                    |
| <span data-ttu-id="f3b0e-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f3b0e-207">Is-Single-Valued</span></span>       | <span data-ttu-id="f3b0e-208">Falso</span><span class="sxs-lookup"><span data-stu-id="f3b0e-208">False</span></span>                                    |
| <span data-ttu-id="f3b0e-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="f3b0e-209">Is Indexed</span></span>             | <span data-ttu-id="f3b0e-210">Falso</span><span class="sxs-lookup"><span data-stu-id="f3b0e-210">False</span></span>                                    |
| <span data-ttu-id="f3b0e-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f3b0e-211">In Global Catalog</span></span>      | <span data-ttu-id="f3b0e-212">Falso</span><span class="sxs-lookup"><span data-stu-id="f3b0e-212">False</span></span>                                    |
| <span data-ttu-id="f3b0e-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f3b0e-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3b0e-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f3b0e-214">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f3b0e-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3b0e-215">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f3b0e-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3b0e-216">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f3b0e-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3b0e-217">Search-Flags</span></span>           | <span data-ttu-id="f3b0e-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3b0e-218">0x00000000</span></span>                               |
| <span data-ttu-id="f3b0e-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3b0e-219">System-Flags</span></span>           | <span data-ttu-id="f3b0e-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f3b0e-220">0x00000010</span></span>                               |
| <span data-ttu-id="f3b0e-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f3b0e-221">Classes used in</span></span>        | [<span data-ttu-id="f3b0e-222">**Nó DNS**</span><span class="sxs-lookup"><span data-stu-id="f3b0e-222">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f3b0e-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f3b0e-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f3b0e-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="f3b0e-224">Entry</span></span> | <span data-ttu-id="f3b0e-225">Valor</span><span class="sxs-lookup"><span data-stu-id="f3b0e-225">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f3b0e-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="f3b0e-226">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="f3b0e-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3b0e-227">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="f3b0e-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3b0e-228">System-Only</span></span>            | <span data-ttu-id="f3b0e-229">Falso</span><span class="sxs-lookup"><span data-stu-id="f3b0e-229">False</span></span>                                    |
| <span data-ttu-id="f3b0e-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f3b0e-230">Is-Single-Valued</span></span>       | <span data-ttu-id="f3b0e-231">Falso</span><span class="sxs-lookup"><span data-stu-id="f3b0e-231">False</span></span>                                    |
| <span data-ttu-id="f3b0e-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="f3b0e-232">Is Indexed</span></span>             | <span data-ttu-id="f3b0e-233">Falso</span><span class="sxs-lookup"><span data-stu-id="f3b0e-233">False</span></span>                                    |
| <span data-ttu-id="f3b0e-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f3b0e-234">In Global Catalog</span></span>      | <span data-ttu-id="f3b0e-235">Falso</span><span class="sxs-lookup"><span data-stu-id="f3b0e-235">False</span></span>                                    |
| <span data-ttu-id="f3b0e-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f3b0e-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3b0e-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f3b0e-237">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f3b0e-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3b0e-238">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f3b0e-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3b0e-239">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f3b0e-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3b0e-240">Search-Flags</span></span>           | <span data-ttu-id="f3b0e-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3b0e-241">0x00000000</span></span>                               |
| <span data-ttu-id="f3b0e-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3b0e-242">System-Flags</span></span>           | <span data-ttu-id="f3b0e-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f3b0e-243">0x00000010</span></span>                               |
| <span data-ttu-id="f3b0e-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f3b0e-244">Classes used in</span></span>        | [<span data-ttu-id="f3b0e-245">**Nó DNS**</span><span class="sxs-lookup"><span data-stu-id="f3b0e-245">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f3b0e-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f3b0e-246">Windows Server 2012</span></span>



| <span data-ttu-id="f3b0e-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="f3b0e-247">Entry</span></span> | <span data-ttu-id="f3b0e-248">Valor</span><span class="sxs-lookup"><span data-stu-id="f3b0e-248">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f3b0e-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="f3b0e-249">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="f3b0e-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f3b0e-250">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="f3b0e-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="f3b0e-251">System-Only</span></span>            | <span data-ttu-id="f3b0e-252">Falso</span><span class="sxs-lookup"><span data-stu-id="f3b0e-252">False</span></span>                                    |
| <span data-ttu-id="f3b0e-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f3b0e-253">Is-Single-Valued</span></span>       | <span data-ttu-id="f3b0e-254">Falso</span><span class="sxs-lookup"><span data-stu-id="f3b0e-254">False</span></span>                                    |
| <span data-ttu-id="f3b0e-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="f3b0e-255">Is Indexed</span></span>             | <span data-ttu-id="f3b0e-256">Falso</span><span class="sxs-lookup"><span data-stu-id="f3b0e-256">False</span></span>                                    |
| <span data-ttu-id="f3b0e-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f3b0e-257">In Global Catalog</span></span>      | <span data-ttu-id="f3b0e-258">Falso</span><span class="sxs-lookup"><span data-stu-id="f3b0e-258">False</span></span>                                    |
| <span data-ttu-id="f3b0e-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f3b0e-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="f3b0e-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f3b0e-260">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f3b0e-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f3b0e-261">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="f3b0e-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f3b0e-262">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="f3b0e-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f3b0e-263">Search-Flags</span></span>           | <span data-ttu-id="f3b0e-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f3b0e-264">0x00000000</span></span>                               |
| <span data-ttu-id="f3b0e-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f3b0e-265">System-Flags</span></span>           | <span data-ttu-id="f3b0e-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f3b0e-266">0x00000010</span></span>                               |
| <span data-ttu-id="f3b0e-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f3b0e-267">Classes used in</span></span>        | [<span data-ttu-id="f3b0e-268">**Nó DNS**</span><span class="sxs-lookup"><span data-stu-id="f3b0e-268">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



 

 





