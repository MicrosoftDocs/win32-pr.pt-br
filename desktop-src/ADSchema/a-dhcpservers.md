---
title: atributo DHCP-Servers
description: Contém uma lista de servidores que são autorizados na empresa.
ms.assetid: f712b2d2-ff9c-4ee2-aede-b68023e3e6b6
ms.tgt_platform: multiple
keywords:
- atributos de AD do atributo DHCP-Servers
- Esquema de AD do atributo dhcpServers
topic_type:
- apiref
api_name:
- dhcp-Servers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e43018c91e5bb495ee39476f07f40756cfcf097
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103919334"
---
# <a name="dhcp-servers-attribute"></a><span data-ttu-id="79eb1-105">atributo DHCP-Servers</span><span class="sxs-lookup"><span data-stu-id="79eb1-105">dhcp-Servers attribute</span></span>

<span data-ttu-id="79eb1-106">Contém uma lista de servidores que são autorizados na empresa.</span><span class="sxs-lookup"><span data-stu-id="79eb1-106">Contains a list of servers that are authorized in the enterprise.</span></span>



| <span data-ttu-id="79eb1-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="79eb1-107">Entry</span></span> | <span data-ttu-id="79eb1-108">Valor</span><span class="sxs-lookup"><span data-stu-id="79eb1-108">Value</span></span> |
|-------------------|--------------------------------------------------------|
| <span data-ttu-id="79eb1-109">CN</span><span class="sxs-lookup"><span data-stu-id="79eb1-109">CN</span></span>                | <span data-ttu-id="79eb1-110">Servidores DHCP</span><span class="sxs-lookup"><span data-stu-id="79eb1-110">dhcp-Servers</span></span>                                           |
| <span data-ttu-id="79eb1-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="79eb1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="79eb1-112">dhcpServers</span><span class="sxs-lookup"><span data-stu-id="79eb1-112">dhcpServers</span></span>                                            |
| <span data-ttu-id="79eb1-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="79eb1-113">Size</span></span>              | \-                                                     |
| <span data-ttu-id="79eb1-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="79eb1-114">Update Privilege</span></span>  | <span data-ttu-id="79eb1-115">Administrador de domínio.</span><span class="sxs-lookup"><span data-stu-id="79eb1-115">Domain administrator.</span></span>                                  |
| <span data-ttu-id="79eb1-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="79eb1-116">Update Frequency</span></span>  | <span data-ttu-id="79eb1-117">Quando um novo servidor é adicionado ou removido da floresta.</span><span class="sxs-lookup"><span data-stu-id="79eb1-117">When a new server is added or removed from the forest.</span></span> |
| <span data-ttu-id="79eb1-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="79eb1-118">Attribute-Id</span></span>      | <span data-ttu-id="79eb1-119">1.2.840.113556.1.4.704</span><span class="sxs-lookup"><span data-stu-id="79eb1-119">1.2.840.113556.1.4.704</span></span>                                 |
| <span data-ttu-id="79eb1-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="79eb1-120">System-Id-Guid</span></span>    | <span data-ttu-id="79eb1-121">963d2745-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="79eb1-121">963d2745-48be-11d1-a9c3-0000f80367c1</span></span>                   |
| <span data-ttu-id="79eb1-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="79eb1-122">Syntax</span></span>            | [<span data-ttu-id="79eb1-123">**Cadeia de caracteres (IA5)**</span><span class="sxs-lookup"><span data-stu-id="79eb1-123">**String(IA5)**</span></span>](s-string-ia5.md)                    |



## <a name="implementations"></a><span data-ttu-id="79eb1-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="79eb1-124">Implementations</span></span>

-   [<span data-ttu-id="79eb1-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="79eb1-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="79eb1-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="79eb1-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="79eb1-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="79eb1-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="79eb1-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="79eb1-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="79eb1-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="79eb1-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="79eb1-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="79eb1-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="79eb1-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="79eb1-131">Windows 2000 Server</span></span>



| <span data-ttu-id="79eb1-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="79eb1-132">Entry</span></span> | <span data-ttu-id="79eb1-133">Valor</span><span class="sxs-lookup"><span data-stu-id="79eb1-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="79eb1-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="79eb1-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="79eb1-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79eb1-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="79eb1-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="79eb1-136">System-Only</span></span>            | <span data-ttu-id="79eb1-137">Falso</span><span class="sxs-lookup"><span data-stu-id="79eb1-137">False</span></span>                                        |
| <span data-ttu-id="79eb1-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="79eb1-138">Is-Single-Valued</span></span>       | <span data-ttu-id="79eb1-139">Falso</span><span class="sxs-lookup"><span data-stu-id="79eb1-139">False</span></span>                                        |
| <span data-ttu-id="79eb1-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="79eb1-140">Is Indexed</span></span>             | <span data-ttu-id="79eb1-141">Falso</span><span class="sxs-lookup"><span data-stu-id="79eb1-141">False</span></span>                                        |
| <span data-ttu-id="79eb1-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="79eb1-142">In Global Catalog</span></span>      | <span data-ttu-id="79eb1-143">Falso</span><span class="sxs-lookup"><span data-stu-id="79eb1-143">False</span></span>                                        |
| <span data-ttu-id="79eb1-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="79eb1-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="79eb1-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="79eb1-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="79eb1-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79eb1-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="79eb1-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79eb1-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="79eb1-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79eb1-148">Search-Flags</span></span>           | <span data-ttu-id="79eb1-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="79eb1-149">0x00000000</span></span>                                   |
| <span data-ttu-id="79eb1-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79eb1-150">System-Flags</span></span>           | <span data-ttu-id="79eb1-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="79eb1-151">0x00000010</span></span>                                   |
| <span data-ttu-id="79eb1-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="79eb1-152">Classes used in</span></span>        | [<span data-ttu-id="79eb1-153">**Classe DHCP**</span><span class="sxs-lookup"><span data-stu-id="79eb1-153">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="79eb1-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="79eb1-154">Windows Server 2003</span></span>



| <span data-ttu-id="79eb1-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="79eb1-155">Entry</span></span> | <span data-ttu-id="79eb1-156">Valor</span><span class="sxs-lookup"><span data-stu-id="79eb1-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="79eb1-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="79eb1-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="79eb1-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79eb1-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="79eb1-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="79eb1-159">System-Only</span></span>            | <span data-ttu-id="79eb1-160">Falso</span><span class="sxs-lookup"><span data-stu-id="79eb1-160">False</span></span>                                        |
| <span data-ttu-id="79eb1-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="79eb1-161">Is-Single-Valued</span></span>       | <span data-ttu-id="79eb1-162">Falso</span><span class="sxs-lookup"><span data-stu-id="79eb1-162">False</span></span>                                        |
| <span data-ttu-id="79eb1-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="79eb1-163">Is Indexed</span></span>             | <span data-ttu-id="79eb1-164">Falso</span><span class="sxs-lookup"><span data-stu-id="79eb1-164">False</span></span>                                        |
| <span data-ttu-id="79eb1-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="79eb1-165">In Global Catalog</span></span>      | <span data-ttu-id="79eb1-166">Falso</span><span class="sxs-lookup"><span data-stu-id="79eb1-166">False</span></span>                                        |
| <span data-ttu-id="79eb1-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="79eb1-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="79eb1-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="79eb1-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="79eb1-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79eb1-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="79eb1-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79eb1-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="79eb1-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79eb1-171">Search-Flags</span></span>           | <span data-ttu-id="79eb1-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="79eb1-172">0x00000000</span></span>                                   |
| <span data-ttu-id="79eb1-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79eb1-173">System-Flags</span></span>           | <span data-ttu-id="79eb1-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="79eb1-174">0x00000010</span></span>                                   |
| <span data-ttu-id="79eb1-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="79eb1-175">Classes used in</span></span>        | [<span data-ttu-id="79eb1-176">**Classe DHCP**</span><span class="sxs-lookup"><span data-stu-id="79eb1-176">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="79eb1-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="79eb1-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="79eb1-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="79eb1-178">Entry</span></span> | <span data-ttu-id="79eb1-179">Valor</span><span class="sxs-lookup"><span data-stu-id="79eb1-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="79eb1-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="79eb1-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="79eb1-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79eb1-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="79eb1-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="79eb1-182">System-Only</span></span>            | <span data-ttu-id="79eb1-183">Falso</span><span class="sxs-lookup"><span data-stu-id="79eb1-183">False</span></span>                                        |
| <span data-ttu-id="79eb1-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="79eb1-184">Is-Single-Valued</span></span>       | <span data-ttu-id="79eb1-185">Falso</span><span class="sxs-lookup"><span data-stu-id="79eb1-185">False</span></span>                                        |
| <span data-ttu-id="79eb1-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="79eb1-186">Is Indexed</span></span>             | <span data-ttu-id="79eb1-187">Falso</span><span class="sxs-lookup"><span data-stu-id="79eb1-187">False</span></span>                                        |
| <span data-ttu-id="79eb1-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="79eb1-188">In Global Catalog</span></span>      | <span data-ttu-id="79eb1-189">Falso</span><span class="sxs-lookup"><span data-stu-id="79eb1-189">False</span></span>                                        |
| <span data-ttu-id="79eb1-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="79eb1-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="79eb1-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="79eb1-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="79eb1-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79eb1-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="79eb1-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79eb1-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="79eb1-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79eb1-194">Search-Flags</span></span>           | <span data-ttu-id="79eb1-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="79eb1-195">0x00000000</span></span>                                   |
| <span data-ttu-id="79eb1-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79eb1-196">System-Flags</span></span>           | <span data-ttu-id="79eb1-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="79eb1-197">0x00000010</span></span>                                   |
| <span data-ttu-id="79eb1-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="79eb1-198">Classes used in</span></span>        | [<span data-ttu-id="79eb1-199">**Classe DHCP**</span><span class="sxs-lookup"><span data-stu-id="79eb1-199">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="79eb1-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="79eb1-200">Windows Server 2008</span></span>



| <span data-ttu-id="79eb1-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="79eb1-201">Entry</span></span> | <span data-ttu-id="79eb1-202">Valor</span><span class="sxs-lookup"><span data-stu-id="79eb1-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="79eb1-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="79eb1-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="79eb1-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79eb1-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="79eb1-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="79eb1-205">System-Only</span></span>            | <span data-ttu-id="79eb1-206">Falso</span><span class="sxs-lookup"><span data-stu-id="79eb1-206">False</span></span>                                        |
| <span data-ttu-id="79eb1-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="79eb1-207">Is-Single-Valued</span></span>       | <span data-ttu-id="79eb1-208">Falso</span><span class="sxs-lookup"><span data-stu-id="79eb1-208">False</span></span>                                        |
| <span data-ttu-id="79eb1-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="79eb1-209">Is Indexed</span></span>             | <span data-ttu-id="79eb1-210">Falso</span><span class="sxs-lookup"><span data-stu-id="79eb1-210">False</span></span>                                        |
| <span data-ttu-id="79eb1-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="79eb1-211">In Global Catalog</span></span>      | <span data-ttu-id="79eb1-212">Falso</span><span class="sxs-lookup"><span data-stu-id="79eb1-212">False</span></span>                                        |
| <span data-ttu-id="79eb1-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="79eb1-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="79eb1-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="79eb1-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="79eb1-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79eb1-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="79eb1-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79eb1-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="79eb1-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79eb1-217">Search-Flags</span></span>           | <span data-ttu-id="79eb1-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="79eb1-218">0x00000000</span></span>                                   |
| <span data-ttu-id="79eb1-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79eb1-219">System-Flags</span></span>           | <span data-ttu-id="79eb1-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="79eb1-220">0x00000010</span></span>                                   |
| <span data-ttu-id="79eb1-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="79eb1-221">Classes used in</span></span>        | [<span data-ttu-id="79eb1-222">**Classe DHCP**</span><span class="sxs-lookup"><span data-stu-id="79eb1-222">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="79eb1-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="79eb1-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="79eb1-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="79eb1-224">Entry</span></span> | <span data-ttu-id="79eb1-225">Valor</span><span class="sxs-lookup"><span data-stu-id="79eb1-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="79eb1-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="79eb1-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="79eb1-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79eb1-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="79eb1-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="79eb1-228">System-Only</span></span>            | <span data-ttu-id="79eb1-229">Falso</span><span class="sxs-lookup"><span data-stu-id="79eb1-229">False</span></span>                                        |
| <span data-ttu-id="79eb1-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="79eb1-230">Is-Single-Valued</span></span>       | <span data-ttu-id="79eb1-231">Falso</span><span class="sxs-lookup"><span data-stu-id="79eb1-231">False</span></span>                                        |
| <span data-ttu-id="79eb1-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="79eb1-232">Is Indexed</span></span>             | <span data-ttu-id="79eb1-233">Falso</span><span class="sxs-lookup"><span data-stu-id="79eb1-233">False</span></span>                                        |
| <span data-ttu-id="79eb1-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="79eb1-234">In Global Catalog</span></span>      | <span data-ttu-id="79eb1-235">Falso</span><span class="sxs-lookup"><span data-stu-id="79eb1-235">False</span></span>                                        |
| <span data-ttu-id="79eb1-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="79eb1-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="79eb1-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="79eb1-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="79eb1-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79eb1-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="79eb1-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79eb1-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="79eb1-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79eb1-240">Search-Flags</span></span>           | <span data-ttu-id="79eb1-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="79eb1-241">0x00000000</span></span>                                   |
| <span data-ttu-id="79eb1-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79eb1-242">System-Flags</span></span>           | <span data-ttu-id="79eb1-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="79eb1-243">0x00000010</span></span>                                   |
| <span data-ttu-id="79eb1-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="79eb1-244">Classes used in</span></span>        | [<span data-ttu-id="79eb1-245">**Classe DHCP**</span><span class="sxs-lookup"><span data-stu-id="79eb1-245">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="79eb1-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="79eb1-246">Windows Server 2012</span></span>



| <span data-ttu-id="79eb1-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="79eb1-247">Entry</span></span> | <span data-ttu-id="79eb1-248">Valor</span><span class="sxs-lookup"><span data-stu-id="79eb1-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="79eb1-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="79eb1-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="79eb1-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79eb1-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="79eb1-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="79eb1-251">System-Only</span></span>            | <span data-ttu-id="79eb1-252">Falso</span><span class="sxs-lookup"><span data-stu-id="79eb1-252">False</span></span>                                        |
| <span data-ttu-id="79eb1-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="79eb1-253">Is-Single-Valued</span></span>       | <span data-ttu-id="79eb1-254">Falso</span><span class="sxs-lookup"><span data-stu-id="79eb1-254">False</span></span>                                        |
| <span data-ttu-id="79eb1-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="79eb1-255">Is Indexed</span></span>             | <span data-ttu-id="79eb1-256">Falso</span><span class="sxs-lookup"><span data-stu-id="79eb1-256">False</span></span>                                        |
| <span data-ttu-id="79eb1-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="79eb1-257">In Global Catalog</span></span>      | <span data-ttu-id="79eb1-258">Falso</span><span class="sxs-lookup"><span data-stu-id="79eb1-258">False</span></span>                                        |
| <span data-ttu-id="79eb1-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="79eb1-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="79eb1-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="79eb1-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="79eb1-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79eb1-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="79eb1-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79eb1-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="79eb1-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79eb1-263">Search-Flags</span></span>           | <span data-ttu-id="79eb1-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="79eb1-264">0x00000000</span></span>                                   |
| <span data-ttu-id="79eb1-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79eb1-265">System-Flags</span></span>           | <span data-ttu-id="79eb1-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="79eb1-266">0x00000010</span></span>                                   |
| <span data-ttu-id="79eb1-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="79eb1-267">Classes used in</span></span>        | [<span data-ttu-id="79eb1-268">**Classe DHCP**</span><span class="sxs-lookup"><span data-stu-id="79eb1-268">**DHCP-Class**</span></span>](c-dhcpclass.md)<br/> |



 

 





