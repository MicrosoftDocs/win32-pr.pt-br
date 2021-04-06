---
title: atributo de tipo DHCP
description: O tipo de servidor DHCP.
ms.assetid: 46ab7db7-a752-45aa-a10b-1195b5cf6f80
ms.tgt_platform: multiple
keywords:
- atributo de AD Schema do tipo DHCP
- atributo dhcptype de AD Schema
topic_type:
- apiref
api_name:
- dhcp-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b5a5a331ff7298854f4ca070799a05e2a3497f2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103919332"
---
# <a name="dhcp-type-attribute"></a><span data-ttu-id="563f8-105">atributo de tipo DHCP</span><span class="sxs-lookup"><span data-stu-id="563f8-105">dhcp-Type attribute</span></span>

<span data-ttu-id="563f8-106">O tipo de servidor DHCP.</span><span class="sxs-lookup"><span data-stu-id="563f8-106">The type of DHCP server.</span></span> <span data-ttu-id="563f8-107">Esse atributo é definido em todos os objetos de objectClass [**dHCPClass**](c-dhcpclass.md).</span><span class="sxs-lookup"><span data-stu-id="563f8-107">This attribute is set on all objects of objectClass [**dHCPClass**](c-dhcpclass.md).</span></span> <span data-ttu-id="563f8-108">Seu valor define o tipo de objeto:</span><span class="sxs-lookup"><span data-stu-id="563f8-108">Its value defines the type of object:</span></span>

``` syntax
  0 - DHCP Root Object
  1 - DHCP Server
```



| <span data-ttu-id="563f8-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="563f8-109">Entry</span></span> | <span data-ttu-id="563f8-110">Valor</span><span class="sxs-lookup"><span data-stu-id="563f8-110">Value</span></span> |
|-------------------|--------------------------------------------------------|
| <span data-ttu-id="563f8-111">CN</span><span class="sxs-lookup"><span data-stu-id="563f8-111">CN</span></span>                | <span data-ttu-id="563f8-112">Tipo de DHCP</span><span class="sxs-lookup"><span data-stu-id="563f8-112">dhcp-Type</span></span>                                              |
| <span data-ttu-id="563f8-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="563f8-113">Ldap-Display-Name</span></span> | <span data-ttu-id="563f8-114">dhcptype</span><span class="sxs-lookup"><span data-stu-id="563f8-114">dhcpType</span></span>                                               |
| <span data-ttu-id="563f8-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="563f8-115">Size</span></span>              | <span data-ttu-id="563f8-116">4 bytes</span><span class="sxs-lookup"><span data-stu-id="563f8-116">4 bytes</span></span>                                                |
| <span data-ttu-id="563f8-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="563f8-117">Update Privilege</span></span>  | <span data-ttu-id="563f8-118">Administrador de domínio.</span><span class="sxs-lookup"><span data-stu-id="563f8-118">Domain administrator.</span></span>                                  |
| <span data-ttu-id="563f8-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="563f8-119">Update Frequency</span></span>  | <span data-ttu-id="563f8-120">Quando um novo servidor é adicionado ou removido da floresta.</span><span class="sxs-lookup"><span data-stu-id="563f8-120">When a new server is added or removed from the forest.</span></span> |
| <span data-ttu-id="563f8-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="563f8-121">Attribute-Id</span></span>      | <span data-ttu-id="563f8-122">1.2.840.113556.1.4.699</span><span class="sxs-lookup"><span data-stu-id="563f8-122">1.2.840.113556.1.4.699</span></span>                                 |
| <span data-ttu-id="563f8-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="563f8-123">System-Id-Guid</span></span>    | <span data-ttu-id="563f8-124">963d273b-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="563f8-124">963d273b-48be-11d1-a9c3-0000f80367c1</span></span>                   |
| <span data-ttu-id="563f8-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="563f8-125">Syntax</span></span>            | [<span data-ttu-id="563f8-126">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="563f8-126">**Enumeration**</span></span>](s-enumeration.md)                   |



## <a name="implementations"></a><span data-ttu-id="563f8-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="563f8-127">Implementations</span></span>

-   [<span data-ttu-id="563f8-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="563f8-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="563f8-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="563f8-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="563f8-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="563f8-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="563f8-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="563f8-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="563f8-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="563f8-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="563f8-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="563f8-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="563f8-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="563f8-134">Windows 2000 Server</span></span>



| <span data-ttu-id="563f8-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="563f8-135">Entry</span></span> | <span data-ttu-id="563f8-136">Valor</span><span class="sxs-lookup"><span data-stu-id="563f8-136">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="563f8-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="563f8-137">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="563f8-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="563f8-138">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="563f8-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="563f8-139">System-Only</span></span>            | <span data-ttu-id="563f8-140">Falso</span><span class="sxs-lookup"><span data-stu-id="563f8-140">False</span></span>                                        |
| <span data-ttu-id="563f8-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="563f8-141">Is-Single-Valued</span></span>       | <span data-ttu-id="563f8-142">True</span><span class="sxs-lookup"><span data-stu-id="563f8-142">True</span></span>                                         |
| <span data-ttu-id="563f8-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="563f8-143">Is Indexed</span></span>             | <span data-ttu-id="563f8-144">True</span><span class="sxs-lookup"><span data-stu-id="563f8-144">True</span></span>                                         |
| <span data-ttu-id="563f8-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="563f8-145">In Global Catalog</span></span>      | <span data-ttu-id="563f8-146">Falso</span><span class="sxs-lookup"><span data-stu-id="563f8-146">False</span></span>                                        |
| <span data-ttu-id="563f8-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="563f8-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="563f8-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="563f8-148">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="563f8-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="563f8-149">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="563f8-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="563f8-150">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="563f8-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="563f8-151">Search-Flags</span></span>           | <span data-ttu-id="563f8-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="563f8-152">0x00000001</span></span>                                   |
| <span data-ttu-id="563f8-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="563f8-153">System-Flags</span></span>           | <span data-ttu-id="563f8-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="563f8-154">0x00000010</span></span>                                   |
| <span data-ttu-id="563f8-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="563f8-155">Classes used in</span></span>        | [<span data-ttu-id="563f8-156">**Classe DHCP**</span><span class="sxs-lookup"><span data-stu-id="563f8-156">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="563f8-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="563f8-157">Windows Server 2003</span></span>



| <span data-ttu-id="563f8-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="563f8-158">Entry</span></span> | <span data-ttu-id="563f8-159">Valor</span><span class="sxs-lookup"><span data-stu-id="563f8-159">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="563f8-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="563f8-160">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="563f8-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="563f8-161">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="563f8-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="563f8-162">System-Only</span></span>            | <span data-ttu-id="563f8-163">Falso</span><span class="sxs-lookup"><span data-stu-id="563f8-163">False</span></span>                                        |
| <span data-ttu-id="563f8-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="563f8-164">Is-Single-Valued</span></span>       | <span data-ttu-id="563f8-165">True</span><span class="sxs-lookup"><span data-stu-id="563f8-165">True</span></span>                                         |
| <span data-ttu-id="563f8-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="563f8-166">Is Indexed</span></span>             | <span data-ttu-id="563f8-167">True</span><span class="sxs-lookup"><span data-stu-id="563f8-167">True</span></span>                                         |
| <span data-ttu-id="563f8-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="563f8-168">In Global Catalog</span></span>      | <span data-ttu-id="563f8-169">Falso</span><span class="sxs-lookup"><span data-stu-id="563f8-169">False</span></span>                                        |
| <span data-ttu-id="563f8-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="563f8-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="563f8-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="563f8-171">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="563f8-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="563f8-172">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="563f8-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="563f8-173">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="563f8-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="563f8-174">Search-Flags</span></span>           | <span data-ttu-id="563f8-175">0x00000001</span><span class="sxs-lookup"><span data-stu-id="563f8-175">0x00000001</span></span>                                   |
| <span data-ttu-id="563f8-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="563f8-176">System-Flags</span></span>           | <span data-ttu-id="563f8-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="563f8-177">0x00000010</span></span>                                   |
| <span data-ttu-id="563f8-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="563f8-178">Classes used in</span></span>        | [<span data-ttu-id="563f8-179">**Classe DHCP**</span><span class="sxs-lookup"><span data-stu-id="563f8-179">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="563f8-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="563f8-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="563f8-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="563f8-181">Entry</span></span> | <span data-ttu-id="563f8-182">Valor</span><span class="sxs-lookup"><span data-stu-id="563f8-182">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="563f8-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="563f8-183">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="563f8-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="563f8-184">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="563f8-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="563f8-185">System-Only</span></span>            | <span data-ttu-id="563f8-186">Falso</span><span class="sxs-lookup"><span data-stu-id="563f8-186">False</span></span>                                        |
| <span data-ttu-id="563f8-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="563f8-187">Is-Single-Valued</span></span>       | <span data-ttu-id="563f8-188">True</span><span class="sxs-lookup"><span data-stu-id="563f8-188">True</span></span>                                         |
| <span data-ttu-id="563f8-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="563f8-189">Is Indexed</span></span>             | <span data-ttu-id="563f8-190">True</span><span class="sxs-lookup"><span data-stu-id="563f8-190">True</span></span>                                         |
| <span data-ttu-id="563f8-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="563f8-191">In Global Catalog</span></span>      | <span data-ttu-id="563f8-192">Falso</span><span class="sxs-lookup"><span data-stu-id="563f8-192">False</span></span>                                        |
| <span data-ttu-id="563f8-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="563f8-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="563f8-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="563f8-194">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="563f8-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="563f8-195">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="563f8-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="563f8-196">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="563f8-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="563f8-197">Search-Flags</span></span>           | <span data-ttu-id="563f8-198">0x00000001</span><span class="sxs-lookup"><span data-stu-id="563f8-198">0x00000001</span></span>                                   |
| <span data-ttu-id="563f8-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="563f8-199">System-Flags</span></span>           | <span data-ttu-id="563f8-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="563f8-200">0x00000010</span></span>                                   |
| <span data-ttu-id="563f8-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="563f8-201">Classes used in</span></span>        | [<span data-ttu-id="563f8-202">**Classe DHCP**</span><span class="sxs-lookup"><span data-stu-id="563f8-202">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="563f8-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="563f8-203">Windows Server 2008</span></span>



| <span data-ttu-id="563f8-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="563f8-204">Entry</span></span> | <span data-ttu-id="563f8-205">Valor</span><span class="sxs-lookup"><span data-stu-id="563f8-205">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="563f8-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="563f8-206">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="563f8-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="563f8-207">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="563f8-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="563f8-208">System-Only</span></span>            | <span data-ttu-id="563f8-209">Falso</span><span class="sxs-lookup"><span data-stu-id="563f8-209">False</span></span>                                        |
| <span data-ttu-id="563f8-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="563f8-210">Is-Single-Valued</span></span>       | <span data-ttu-id="563f8-211">True</span><span class="sxs-lookup"><span data-stu-id="563f8-211">True</span></span>                                         |
| <span data-ttu-id="563f8-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="563f8-212">Is Indexed</span></span>             | <span data-ttu-id="563f8-213">True</span><span class="sxs-lookup"><span data-stu-id="563f8-213">True</span></span>                                         |
| <span data-ttu-id="563f8-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="563f8-214">In Global Catalog</span></span>      | <span data-ttu-id="563f8-215">Falso</span><span class="sxs-lookup"><span data-stu-id="563f8-215">False</span></span>                                        |
| <span data-ttu-id="563f8-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="563f8-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="563f8-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="563f8-217">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="563f8-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="563f8-218">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="563f8-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="563f8-219">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="563f8-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="563f8-220">Search-Flags</span></span>           | <span data-ttu-id="563f8-221">0x00000001</span><span class="sxs-lookup"><span data-stu-id="563f8-221">0x00000001</span></span>                                   |
| <span data-ttu-id="563f8-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="563f8-222">System-Flags</span></span>           | <span data-ttu-id="563f8-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="563f8-223">0x00000010</span></span>                                   |
| <span data-ttu-id="563f8-224">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="563f8-224">Classes used in</span></span>        | [<span data-ttu-id="563f8-225">**Classe DHCP**</span><span class="sxs-lookup"><span data-stu-id="563f8-225">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="563f8-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="563f8-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="563f8-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="563f8-227">Entry</span></span> | <span data-ttu-id="563f8-228">Valor</span><span class="sxs-lookup"><span data-stu-id="563f8-228">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="563f8-229">ID do link</span><span class="sxs-lookup"><span data-stu-id="563f8-229">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="563f8-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="563f8-230">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="563f8-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="563f8-231">System-Only</span></span>            | <span data-ttu-id="563f8-232">Falso</span><span class="sxs-lookup"><span data-stu-id="563f8-232">False</span></span>                                        |
| <span data-ttu-id="563f8-233">É de valor único</span><span class="sxs-lookup"><span data-stu-id="563f8-233">Is-Single-Valued</span></span>       | <span data-ttu-id="563f8-234">True</span><span class="sxs-lookup"><span data-stu-id="563f8-234">True</span></span>                                         |
| <span data-ttu-id="563f8-235">É indexado</span><span class="sxs-lookup"><span data-stu-id="563f8-235">Is Indexed</span></span>             | <span data-ttu-id="563f8-236">True</span><span class="sxs-lookup"><span data-stu-id="563f8-236">True</span></span>                                         |
| <span data-ttu-id="563f8-237">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="563f8-237">In Global Catalog</span></span>      | <span data-ttu-id="563f8-238">Falso</span><span class="sxs-lookup"><span data-stu-id="563f8-238">False</span></span>                                        |
| <span data-ttu-id="563f8-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="563f8-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="563f8-240">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="563f8-240">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="563f8-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="563f8-241">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="563f8-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="563f8-242">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="563f8-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="563f8-243">Search-Flags</span></span>           | <span data-ttu-id="563f8-244">0x00000001</span><span class="sxs-lookup"><span data-stu-id="563f8-244">0x00000001</span></span>                                   |
| <span data-ttu-id="563f8-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="563f8-245">System-Flags</span></span>           | <span data-ttu-id="563f8-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="563f8-246">0x00000010</span></span>                                   |
| <span data-ttu-id="563f8-247">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="563f8-247">Classes used in</span></span>        | [<span data-ttu-id="563f8-248">**Classe DHCP**</span><span class="sxs-lookup"><span data-stu-id="563f8-248">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="563f8-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="563f8-249">Windows Server 2012</span></span>



| <span data-ttu-id="563f8-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="563f8-250">Entry</span></span> | <span data-ttu-id="563f8-251">Valor</span><span class="sxs-lookup"><span data-stu-id="563f8-251">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="563f8-252">ID do link</span><span class="sxs-lookup"><span data-stu-id="563f8-252">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="563f8-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="563f8-253">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="563f8-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="563f8-254">System-Only</span></span>            | <span data-ttu-id="563f8-255">Falso</span><span class="sxs-lookup"><span data-stu-id="563f8-255">False</span></span>                                        |
| <span data-ttu-id="563f8-256">É de valor único</span><span class="sxs-lookup"><span data-stu-id="563f8-256">Is-Single-Valued</span></span>       | <span data-ttu-id="563f8-257">True</span><span class="sxs-lookup"><span data-stu-id="563f8-257">True</span></span>                                         |
| <span data-ttu-id="563f8-258">É indexado</span><span class="sxs-lookup"><span data-stu-id="563f8-258">Is Indexed</span></span>             | <span data-ttu-id="563f8-259">True</span><span class="sxs-lookup"><span data-stu-id="563f8-259">True</span></span>                                         |
| <span data-ttu-id="563f8-260">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="563f8-260">In Global Catalog</span></span>      | <span data-ttu-id="563f8-261">Falso</span><span class="sxs-lookup"><span data-stu-id="563f8-261">False</span></span>                                        |
| <span data-ttu-id="563f8-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="563f8-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="563f8-263">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="563f8-263">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="563f8-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="563f8-264">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="563f8-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="563f8-265">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="563f8-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="563f8-266">Search-Flags</span></span>           | <span data-ttu-id="563f8-267">0x00000001</span><span class="sxs-lookup"><span data-stu-id="563f8-267">0x00000001</span></span>                                   |
| <span data-ttu-id="563f8-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="563f8-268">System-Flags</span></span>           | <span data-ttu-id="563f8-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="563f8-269">0x00000010</span></span>                                   |
| <span data-ttu-id="563f8-270">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="563f8-270">Classes used in</span></span>        | [<span data-ttu-id="563f8-271">**Classe DHCP**</span><span class="sxs-lookup"><span data-stu-id="563f8-271">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



 

 





