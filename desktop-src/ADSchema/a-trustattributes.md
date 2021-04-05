---
title: Trust-Attributes atributo
description: Esse atributo armazena os atributos de confiança para um domínio confiável.
ms.assetid: c85b98a6-4d09-4eb2-821b-58ef558b3460
ms.tgt_platform: multiple
keywords:
- Esquema de Trust-Attributes do atributo AD
- Esquema de AD do atributo trustattributes
topic_type:
- apiref
api_name:
- Trust-Attributes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d81dc06f73fbda5dab7ce8d2a07bfc90323d2b29
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645495"
---
# <a name="trust-attributes-attribute"></a><span data-ttu-id="85a7f-105">Trust-Attributes atributo</span><span class="sxs-lookup"><span data-stu-id="85a7f-105">Trust-Attributes attribute</span></span>

<span data-ttu-id="85a7f-106">Esse atributo armazena os atributos de confiança para um domínio confiável.</span><span class="sxs-lookup"><span data-stu-id="85a7f-106">This attribute stores the trust attributes for a trusted domain.</span></span> <span data-ttu-id="85a7f-107">Os valores de atributo possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="85a7f-107">Possible attribute values are as follows:</span></span>

-   <span data-ttu-id="85a7f-108">Atributo de confiança \_ \_ não \_ transitiva desabilite transitividade.</span><span class="sxs-lookup"><span data-stu-id="85a7f-108">TRUST\_ATTRIBUTE\_NON\_TRANSITIVE Disable transitivity.</span></span>
-   <span data-ttu-id="85a7f-109">A \_ relação \_ \_ de confiança pai da árvore de atributos de confiança está definida como pai da árvore organizacional.</span><span class="sxs-lookup"><span data-stu-id="85a7f-109">TRUST\_ATTRIBUTE\_TREE\_PARENT Trust is set to the organization tree parent.</span></span>
-   <span data-ttu-id="85a7f-110">Confiança \_ raiz da árvore de atributos de confiança \_ \_ definida como outra raiz da árvore na floresta.</span><span class="sxs-lookup"><span data-stu-id="85a7f-110">TRUST\_ATTRIBUTE\_TREE\_ROOT Trust set to another tree root in the forest.</span></span>
-   <span data-ttu-id="85a7f-111">O \_ atributo de confiança \_ somente o \_ link confiável é válido somente para o cliente de upLevel.</span><span class="sxs-lookup"><span data-stu-id="85a7f-111">TRUST\_ATTRIBUTE\_UPLEVEL\_ONLY Trusted link valid only for uplevel client.</span></span>



| <span data-ttu-id="85a7f-112">Entrada</span><span class="sxs-lookup"><span data-stu-id="85a7f-112">Entry</span></span> | <span data-ttu-id="85a7f-113">Valor</span><span class="sxs-lookup"><span data-stu-id="85a7f-113">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="85a7f-114">CN</span><span class="sxs-lookup"><span data-stu-id="85a7f-114">CN</span></span>                | <span data-ttu-id="85a7f-115">Trust-Attributes</span><span class="sxs-lookup"><span data-stu-id="85a7f-115">Trust-Attributes</span></span>                     |
| <span data-ttu-id="85a7f-116">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="85a7f-116">Ldap-Display-Name</span></span> | <span data-ttu-id="85a7f-117">trustattributes</span><span class="sxs-lookup"><span data-stu-id="85a7f-117">trustAttributes</span></span>                      |
| <span data-ttu-id="85a7f-118">Tamanho</span><span class="sxs-lookup"><span data-stu-id="85a7f-118">Size</span></span>              | \-                                   |
| <span data-ttu-id="85a7f-119">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="85a7f-119">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="85a7f-120">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="85a7f-120">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="85a7f-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="85a7f-121">Attribute-Id</span></span>      | <span data-ttu-id="85a7f-122">1.2.840.113556.1.4.470</span><span class="sxs-lookup"><span data-stu-id="85a7f-122">1.2.840.113556.1.4.470</span></span>               |
| <span data-ttu-id="85a7f-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="85a7f-123">System-Id-Guid</span></span>    | <span data-ttu-id="85a7f-124">80a67e5a-9f22-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="85a7f-124">80a67e5a-9f22-11d0-afdd-00c04fd930c9</span></span> |
| <span data-ttu-id="85a7f-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="85a7f-125">Syntax</span></span>            | [<span data-ttu-id="85a7f-126">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="85a7f-126">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="85a7f-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="85a7f-127">Implementations</span></span>

-   [<span data-ttu-id="85a7f-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="85a7f-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="85a7f-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="85a7f-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="85a7f-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="85a7f-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="85a7f-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="85a7f-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="85a7f-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="85a7f-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="85a7f-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="85a7f-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="85a7f-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="85a7f-134">Windows 2000 Server</span></span>



| <span data-ttu-id="85a7f-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="85a7f-135">Entry</span></span> | <span data-ttu-id="85a7f-136">Valor</span><span class="sxs-lookup"><span data-stu-id="85a7f-136">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="85a7f-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="85a7f-137">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="85a7f-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85a7f-138">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="85a7f-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="85a7f-139">System-Only</span></span>            | <span data-ttu-id="85a7f-140">Falso</span><span class="sxs-lookup"><span data-stu-id="85a7f-140">False</span></span>                                                |
| <span data-ttu-id="85a7f-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="85a7f-141">Is-Single-Valued</span></span>       | <span data-ttu-id="85a7f-142">True</span><span class="sxs-lookup"><span data-stu-id="85a7f-142">True</span></span>                                                 |
| <span data-ttu-id="85a7f-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="85a7f-143">Is Indexed</span></span>             | <span data-ttu-id="85a7f-144">Falso</span><span class="sxs-lookup"><span data-stu-id="85a7f-144">False</span></span>                                                |
| <span data-ttu-id="85a7f-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="85a7f-145">In Global Catalog</span></span>      | <span data-ttu-id="85a7f-146">Falso</span><span class="sxs-lookup"><span data-stu-id="85a7f-146">False</span></span>                                                |
| <span data-ttu-id="85a7f-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="85a7f-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="85a7f-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="85a7f-148">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="85a7f-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85a7f-149">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="85a7f-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85a7f-150">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="85a7f-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85a7f-151">Search-Flags</span></span>           | <span data-ttu-id="85a7f-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85a7f-152">0x00000000</span></span>                                           |
| <span data-ttu-id="85a7f-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85a7f-153">System-Flags</span></span>           | <span data-ttu-id="85a7f-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="85a7f-154">0x00000010</span></span>                                           |
| <span data-ttu-id="85a7f-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="85a7f-155">Classes used in</span></span>        | [<span data-ttu-id="85a7f-156">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="85a7f-156">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="85a7f-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="85a7f-157">Windows Server 2003</span></span>



| <span data-ttu-id="85a7f-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="85a7f-158">Entry</span></span> | <span data-ttu-id="85a7f-159">Valor</span><span class="sxs-lookup"><span data-stu-id="85a7f-159">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="85a7f-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="85a7f-160">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="85a7f-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85a7f-161">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="85a7f-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="85a7f-162">System-Only</span></span>            | <span data-ttu-id="85a7f-163">Falso</span><span class="sxs-lookup"><span data-stu-id="85a7f-163">False</span></span>                                                |
| <span data-ttu-id="85a7f-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="85a7f-164">Is-Single-Valued</span></span>       | <span data-ttu-id="85a7f-165">True</span><span class="sxs-lookup"><span data-stu-id="85a7f-165">True</span></span>                                                 |
| <span data-ttu-id="85a7f-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="85a7f-166">Is Indexed</span></span>             | <span data-ttu-id="85a7f-167">Falso</span><span class="sxs-lookup"><span data-stu-id="85a7f-167">False</span></span>                                                |
| <span data-ttu-id="85a7f-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="85a7f-168">In Global Catalog</span></span>      | <span data-ttu-id="85a7f-169">True</span><span class="sxs-lookup"><span data-stu-id="85a7f-169">True</span></span>                                                 |
| <span data-ttu-id="85a7f-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="85a7f-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="85a7f-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="85a7f-171">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="85a7f-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85a7f-172">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="85a7f-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85a7f-173">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="85a7f-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85a7f-174">Search-Flags</span></span>           | <span data-ttu-id="85a7f-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85a7f-175">0x00000000</span></span>                                           |
| <span data-ttu-id="85a7f-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85a7f-176">System-Flags</span></span>           | <span data-ttu-id="85a7f-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="85a7f-177">0x00000010</span></span>                                           |
| <span data-ttu-id="85a7f-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="85a7f-178">Classes used in</span></span>        | [<span data-ttu-id="85a7f-179">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="85a7f-179">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="85a7f-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="85a7f-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="85a7f-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="85a7f-181">Entry</span></span> | <span data-ttu-id="85a7f-182">Valor</span><span class="sxs-lookup"><span data-stu-id="85a7f-182">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="85a7f-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="85a7f-183">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="85a7f-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85a7f-184">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="85a7f-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="85a7f-185">System-Only</span></span>            | <span data-ttu-id="85a7f-186">Falso</span><span class="sxs-lookup"><span data-stu-id="85a7f-186">False</span></span>                                                |
| <span data-ttu-id="85a7f-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="85a7f-187">Is-Single-Valued</span></span>       | <span data-ttu-id="85a7f-188">True</span><span class="sxs-lookup"><span data-stu-id="85a7f-188">True</span></span>                                                 |
| <span data-ttu-id="85a7f-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="85a7f-189">Is Indexed</span></span>             | <span data-ttu-id="85a7f-190">Falso</span><span class="sxs-lookup"><span data-stu-id="85a7f-190">False</span></span>                                                |
| <span data-ttu-id="85a7f-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="85a7f-191">In Global Catalog</span></span>      | <span data-ttu-id="85a7f-192">True</span><span class="sxs-lookup"><span data-stu-id="85a7f-192">True</span></span>                                                 |
| <span data-ttu-id="85a7f-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="85a7f-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="85a7f-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="85a7f-194">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="85a7f-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85a7f-195">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="85a7f-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85a7f-196">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="85a7f-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85a7f-197">Search-Flags</span></span>           | <span data-ttu-id="85a7f-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85a7f-198">0x00000000</span></span>                                           |
| <span data-ttu-id="85a7f-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85a7f-199">System-Flags</span></span>           | <span data-ttu-id="85a7f-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="85a7f-200">0x00000010</span></span>                                           |
| <span data-ttu-id="85a7f-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="85a7f-201">Classes used in</span></span>        | [<span data-ttu-id="85a7f-202">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="85a7f-202">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="85a7f-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="85a7f-203">Windows Server 2008</span></span>



| <span data-ttu-id="85a7f-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="85a7f-204">Entry</span></span> | <span data-ttu-id="85a7f-205">Valor</span><span class="sxs-lookup"><span data-stu-id="85a7f-205">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="85a7f-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="85a7f-206">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="85a7f-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85a7f-207">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="85a7f-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="85a7f-208">System-Only</span></span>            | <span data-ttu-id="85a7f-209">Falso</span><span class="sxs-lookup"><span data-stu-id="85a7f-209">False</span></span>                                                |
| <span data-ttu-id="85a7f-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="85a7f-210">Is-Single-Valued</span></span>       | <span data-ttu-id="85a7f-211">True</span><span class="sxs-lookup"><span data-stu-id="85a7f-211">True</span></span>                                                 |
| <span data-ttu-id="85a7f-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="85a7f-212">Is Indexed</span></span>             | <span data-ttu-id="85a7f-213">Falso</span><span class="sxs-lookup"><span data-stu-id="85a7f-213">False</span></span>                                                |
| <span data-ttu-id="85a7f-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="85a7f-214">In Global Catalog</span></span>      | <span data-ttu-id="85a7f-215">True</span><span class="sxs-lookup"><span data-stu-id="85a7f-215">True</span></span>                                                 |
| <span data-ttu-id="85a7f-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="85a7f-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="85a7f-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="85a7f-217">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="85a7f-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85a7f-218">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="85a7f-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85a7f-219">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="85a7f-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85a7f-220">Search-Flags</span></span>           | <span data-ttu-id="85a7f-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85a7f-221">0x00000000</span></span>                                           |
| <span data-ttu-id="85a7f-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85a7f-222">System-Flags</span></span>           | <span data-ttu-id="85a7f-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="85a7f-223">0x00000010</span></span>                                           |
| <span data-ttu-id="85a7f-224">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="85a7f-224">Classes used in</span></span>        | [<span data-ttu-id="85a7f-225">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="85a7f-225">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="85a7f-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="85a7f-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="85a7f-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="85a7f-227">Entry</span></span> | <span data-ttu-id="85a7f-228">Valor</span><span class="sxs-lookup"><span data-stu-id="85a7f-228">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="85a7f-229">ID do link</span><span class="sxs-lookup"><span data-stu-id="85a7f-229">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="85a7f-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85a7f-230">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="85a7f-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="85a7f-231">System-Only</span></span>            | <span data-ttu-id="85a7f-232">Falso</span><span class="sxs-lookup"><span data-stu-id="85a7f-232">False</span></span>                                                |
| <span data-ttu-id="85a7f-233">É de valor único</span><span class="sxs-lookup"><span data-stu-id="85a7f-233">Is-Single-Valued</span></span>       | <span data-ttu-id="85a7f-234">True</span><span class="sxs-lookup"><span data-stu-id="85a7f-234">True</span></span>                                                 |
| <span data-ttu-id="85a7f-235">É indexado</span><span class="sxs-lookup"><span data-stu-id="85a7f-235">Is Indexed</span></span>             | <span data-ttu-id="85a7f-236">Falso</span><span class="sxs-lookup"><span data-stu-id="85a7f-236">False</span></span>                                                |
| <span data-ttu-id="85a7f-237">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="85a7f-237">In Global Catalog</span></span>      | <span data-ttu-id="85a7f-238">True</span><span class="sxs-lookup"><span data-stu-id="85a7f-238">True</span></span>                                                 |
| <span data-ttu-id="85a7f-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="85a7f-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="85a7f-240">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="85a7f-240">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="85a7f-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85a7f-241">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="85a7f-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85a7f-242">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="85a7f-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85a7f-243">Search-Flags</span></span>           | <span data-ttu-id="85a7f-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85a7f-244">0x00000000</span></span>                                           |
| <span data-ttu-id="85a7f-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85a7f-245">System-Flags</span></span>           | <span data-ttu-id="85a7f-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="85a7f-246">0x00000010</span></span>                                           |
| <span data-ttu-id="85a7f-247">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="85a7f-247">Classes used in</span></span>        | [<span data-ttu-id="85a7f-248">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="85a7f-248">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="85a7f-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="85a7f-249">Windows Server 2012</span></span>



| <span data-ttu-id="85a7f-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="85a7f-250">Entry</span></span> | <span data-ttu-id="85a7f-251">Valor</span><span class="sxs-lookup"><span data-stu-id="85a7f-251">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="85a7f-252">ID do link</span><span class="sxs-lookup"><span data-stu-id="85a7f-252">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="85a7f-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="85a7f-253">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="85a7f-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="85a7f-254">System-Only</span></span>            | <span data-ttu-id="85a7f-255">Falso</span><span class="sxs-lookup"><span data-stu-id="85a7f-255">False</span></span>                                                |
| <span data-ttu-id="85a7f-256">É de valor único</span><span class="sxs-lookup"><span data-stu-id="85a7f-256">Is-Single-Valued</span></span>       | <span data-ttu-id="85a7f-257">True</span><span class="sxs-lookup"><span data-stu-id="85a7f-257">True</span></span>                                                 |
| <span data-ttu-id="85a7f-258">É indexado</span><span class="sxs-lookup"><span data-stu-id="85a7f-258">Is Indexed</span></span>             | <span data-ttu-id="85a7f-259">Falso</span><span class="sxs-lookup"><span data-stu-id="85a7f-259">False</span></span>                                                |
| <span data-ttu-id="85a7f-260">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="85a7f-260">In Global Catalog</span></span>      | <span data-ttu-id="85a7f-261">True</span><span class="sxs-lookup"><span data-stu-id="85a7f-261">True</span></span>                                                 |
| <span data-ttu-id="85a7f-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="85a7f-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="85a7f-263">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="85a7f-263">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="85a7f-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="85a7f-264">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="85a7f-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="85a7f-265">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="85a7f-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="85a7f-266">Search-Flags</span></span>           | <span data-ttu-id="85a7f-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85a7f-267">0x00000000</span></span>                                           |
| <span data-ttu-id="85a7f-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="85a7f-268">System-Flags</span></span>           | <span data-ttu-id="85a7f-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="85a7f-269">0x00000010</span></span>                                           |
| <span data-ttu-id="85a7f-270">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="85a7f-270">Classes used in</span></span>        | [<span data-ttu-id="85a7f-271">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="85a7f-271">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





