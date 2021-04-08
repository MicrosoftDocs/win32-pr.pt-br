---
title: Atributo MSMQ-out-Routing-Servers
description: Links de DN para servidores de roteamento MSMQ por meio do qual todo o tráfego de saída deste computador deve ser roteado.
ms.assetid: 169558e4-d2a6-4555-bc5f-7e6a89e51789
ms.tgt_platform: multiple
keywords:
- Atributo AD do MSMQ-out-Routing-Servers
- Esquema de AD do atributo mSMQOutRoutingServers
topic_type:
- apiref
api_name:
- MSMQ-Out-Routing-Servers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfc2265b2d809b7a73cd19faace87473552471a3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825167"
---
# <a name="msmq-out-routing-servers-attribute"></a><span data-ttu-id="c7b87-105">Atributo MSMQ-out-Routing-Servers</span><span class="sxs-lookup"><span data-stu-id="c7b87-105">MSMQ-Out-Routing-Servers attribute</span></span>

<span data-ttu-id="c7b87-106">Links de DN para servidores de roteamento MSMQ por meio do qual todo o tráfego de saída deste computador deve ser roteado.</span><span class="sxs-lookup"><span data-stu-id="c7b87-106">DN links to MSMQ routing servers through which all outgoing traffic for this computer should be routed.</span></span>



| <span data-ttu-id="c7b87-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="c7b87-107">Entry</span></span> | <span data-ttu-id="c7b87-108">Valor</span><span class="sxs-lookup"><span data-stu-id="c7b87-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="c7b87-109">CN</span><span class="sxs-lookup"><span data-stu-id="c7b87-109">CN</span></span>                | <span data-ttu-id="c7b87-110">MSMQ-out-Routing-Servers</span><span class="sxs-lookup"><span data-stu-id="c7b87-110">MSMQ-Out-Routing-Servers</span></span>                |
| <span data-ttu-id="c7b87-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c7b87-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c7b87-112">mSMQOutRoutingServers</span><span class="sxs-lookup"><span data-stu-id="c7b87-112">mSMQOutRoutingServers</span></span>                   |
| <span data-ttu-id="c7b87-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="c7b87-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="c7b87-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="c7b87-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="c7b87-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="c7b87-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="c7b87-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c7b87-116">Attribute-Id</span></span>      | <span data-ttu-id="c7b87-117">1.2.840.113556.1.4.928</span><span class="sxs-lookup"><span data-stu-id="c7b87-117">1.2.840.113556.1.4.928</span></span>                  |
| <span data-ttu-id="c7b87-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c7b87-118">System-Id-Guid</span></span>    | <span data-ttu-id="c7b87-119">9a0dc32b-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="c7b87-119">9a0dc32b-c100-11d1-bbc5-0080c76670c0</span></span>    |
| <span data-ttu-id="c7b87-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7b87-120">Syntax</span></span>            | [<span data-ttu-id="c7b87-121">**Objeto (DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="c7b87-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="c7b87-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="c7b87-122">Implementations</span></span>

-   [<span data-ttu-id="c7b87-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c7b87-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c7b87-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c7b87-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c7b87-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c7b87-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c7b87-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c7b87-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c7b87-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c7b87-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c7b87-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c7b87-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c7b87-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c7b87-129">Windows 2000 Server</span></span>



| <span data-ttu-id="c7b87-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="c7b87-130">Entry</span></span> | <span data-ttu-id="c7b87-131">Valor</span><span class="sxs-lookup"><span data-stu-id="c7b87-131">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="c7b87-132">ID do link</span><span class="sxs-lookup"><span data-stu-id="c7b87-132">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c7b87-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c7b87-133">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c7b87-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="c7b87-134">System-Only</span></span>            | <span data-ttu-id="c7b87-135">Falso</span><span class="sxs-lookup"><span data-stu-id="c7b87-135">False</span></span>                                                        |
| <span data-ttu-id="c7b87-136">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c7b87-136">Is-Single-Valued</span></span>       | <span data-ttu-id="c7b87-137">Falso</span><span class="sxs-lookup"><span data-stu-id="c7b87-137">False</span></span>                                                        |
| <span data-ttu-id="c7b87-138">É indexado</span><span class="sxs-lookup"><span data-stu-id="c7b87-138">Is Indexed</span></span>             | <span data-ttu-id="c7b87-139">Falso</span><span class="sxs-lookup"><span data-stu-id="c7b87-139">False</span></span>                                                        |
| <span data-ttu-id="c7b87-140">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c7b87-140">In Global Catalog</span></span>      | <span data-ttu-id="c7b87-141">True</span><span class="sxs-lookup"><span data-stu-id="c7b87-141">True</span></span>                                                         |
| <span data-ttu-id="c7b87-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c7b87-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="c7b87-143">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c7b87-143">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="c7b87-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c7b87-144">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="c7b87-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c7b87-145">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="c7b87-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c7b87-146">Search-Flags</span></span>           | <span data-ttu-id="c7b87-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c7b87-147">0x00000000</span></span>                                                   |
| <span data-ttu-id="c7b87-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c7b87-148">System-Flags</span></span>           | <span data-ttu-id="c7b87-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c7b87-149">0x00000010</span></span>                                                   |
| <span data-ttu-id="c7b87-150">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c7b87-150">Classes used in</span></span>        | [<span data-ttu-id="c7b87-151">**Configuração do MSMQ**</span><span class="sxs-lookup"><span data-stu-id="c7b87-151">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c7b87-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c7b87-152">Windows Server 2003</span></span>



| <span data-ttu-id="c7b87-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="c7b87-153">Entry</span></span> | <span data-ttu-id="c7b87-154">Valor</span><span class="sxs-lookup"><span data-stu-id="c7b87-154">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="c7b87-155">ID do link</span><span class="sxs-lookup"><span data-stu-id="c7b87-155">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c7b87-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c7b87-156">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c7b87-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="c7b87-157">System-Only</span></span>            | <span data-ttu-id="c7b87-158">Falso</span><span class="sxs-lookup"><span data-stu-id="c7b87-158">False</span></span>                                                        |
| <span data-ttu-id="c7b87-159">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c7b87-159">Is-Single-Valued</span></span>       | <span data-ttu-id="c7b87-160">Falso</span><span class="sxs-lookup"><span data-stu-id="c7b87-160">False</span></span>                                                        |
| <span data-ttu-id="c7b87-161">É indexado</span><span class="sxs-lookup"><span data-stu-id="c7b87-161">Is Indexed</span></span>             | <span data-ttu-id="c7b87-162">Falso</span><span class="sxs-lookup"><span data-stu-id="c7b87-162">False</span></span>                                                        |
| <span data-ttu-id="c7b87-163">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c7b87-163">In Global Catalog</span></span>      | <span data-ttu-id="c7b87-164">True</span><span class="sxs-lookup"><span data-stu-id="c7b87-164">True</span></span>                                                         |
| <span data-ttu-id="c7b87-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c7b87-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="c7b87-166">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c7b87-166">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="c7b87-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c7b87-167">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="c7b87-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c7b87-168">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="c7b87-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c7b87-169">Search-Flags</span></span>           | <span data-ttu-id="c7b87-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c7b87-170">0x00000000</span></span>                                                   |
| <span data-ttu-id="c7b87-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c7b87-171">System-Flags</span></span>           | <span data-ttu-id="c7b87-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c7b87-172">0x00000010</span></span>                                                   |
| <span data-ttu-id="c7b87-173">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c7b87-173">Classes used in</span></span>        | [<span data-ttu-id="c7b87-174">**Configuração do MSMQ**</span><span class="sxs-lookup"><span data-stu-id="c7b87-174">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c7b87-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c7b87-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c7b87-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="c7b87-176">Entry</span></span> | <span data-ttu-id="c7b87-177">Valor</span><span class="sxs-lookup"><span data-stu-id="c7b87-177">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="c7b87-178">ID do link</span><span class="sxs-lookup"><span data-stu-id="c7b87-178">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c7b87-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c7b87-179">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c7b87-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="c7b87-180">System-Only</span></span>            | <span data-ttu-id="c7b87-181">Falso</span><span class="sxs-lookup"><span data-stu-id="c7b87-181">False</span></span>                                                        |
| <span data-ttu-id="c7b87-182">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c7b87-182">Is-Single-Valued</span></span>       | <span data-ttu-id="c7b87-183">Falso</span><span class="sxs-lookup"><span data-stu-id="c7b87-183">False</span></span>                                                        |
| <span data-ttu-id="c7b87-184">É indexado</span><span class="sxs-lookup"><span data-stu-id="c7b87-184">Is Indexed</span></span>             | <span data-ttu-id="c7b87-185">Falso</span><span class="sxs-lookup"><span data-stu-id="c7b87-185">False</span></span>                                                        |
| <span data-ttu-id="c7b87-186">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c7b87-186">In Global Catalog</span></span>      | <span data-ttu-id="c7b87-187">True</span><span class="sxs-lookup"><span data-stu-id="c7b87-187">True</span></span>                                                         |
| <span data-ttu-id="c7b87-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c7b87-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="c7b87-189">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c7b87-189">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="c7b87-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c7b87-190">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="c7b87-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c7b87-191">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="c7b87-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c7b87-192">Search-Flags</span></span>           | <span data-ttu-id="c7b87-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c7b87-193">0x00000000</span></span>                                                   |
| <span data-ttu-id="c7b87-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c7b87-194">System-Flags</span></span>           | <span data-ttu-id="c7b87-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c7b87-195">0x00000010</span></span>                                                   |
| <span data-ttu-id="c7b87-196">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c7b87-196">Classes used in</span></span>        | [<span data-ttu-id="c7b87-197">**Configuração do MSMQ**</span><span class="sxs-lookup"><span data-stu-id="c7b87-197">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c7b87-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7b87-198">Windows Server 2008</span></span>



| <span data-ttu-id="c7b87-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="c7b87-199">Entry</span></span> | <span data-ttu-id="c7b87-200">Valor</span><span class="sxs-lookup"><span data-stu-id="c7b87-200">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="c7b87-201">ID do link</span><span class="sxs-lookup"><span data-stu-id="c7b87-201">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c7b87-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c7b87-202">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c7b87-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="c7b87-203">System-Only</span></span>            | <span data-ttu-id="c7b87-204">Falso</span><span class="sxs-lookup"><span data-stu-id="c7b87-204">False</span></span>                                                        |
| <span data-ttu-id="c7b87-205">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c7b87-205">Is-Single-Valued</span></span>       | <span data-ttu-id="c7b87-206">Falso</span><span class="sxs-lookup"><span data-stu-id="c7b87-206">False</span></span>                                                        |
| <span data-ttu-id="c7b87-207">É indexado</span><span class="sxs-lookup"><span data-stu-id="c7b87-207">Is Indexed</span></span>             | <span data-ttu-id="c7b87-208">Falso</span><span class="sxs-lookup"><span data-stu-id="c7b87-208">False</span></span>                                                        |
| <span data-ttu-id="c7b87-209">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c7b87-209">In Global Catalog</span></span>      | <span data-ttu-id="c7b87-210">True</span><span class="sxs-lookup"><span data-stu-id="c7b87-210">True</span></span>                                                         |
| <span data-ttu-id="c7b87-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c7b87-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="c7b87-212">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c7b87-212">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="c7b87-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c7b87-213">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="c7b87-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c7b87-214">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="c7b87-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c7b87-215">Search-Flags</span></span>           | <span data-ttu-id="c7b87-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c7b87-216">0x00000000</span></span>                                                   |
| <span data-ttu-id="c7b87-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c7b87-217">System-Flags</span></span>           | <span data-ttu-id="c7b87-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c7b87-218">0x00000010</span></span>                                                   |
| <span data-ttu-id="c7b87-219">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c7b87-219">Classes used in</span></span>        | [<span data-ttu-id="c7b87-220">**Configuração do MSMQ**</span><span class="sxs-lookup"><span data-stu-id="c7b87-220">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c7b87-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c7b87-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c7b87-222">Entrada</span><span class="sxs-lookup"><span data-stu-id="c7b87-222">Entry</span></span> | <span data-ttu-id="c7b87-223">Valor</span><span class="sxs-lookup"><span data-stu-id="c7b87-223">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="c7b87-224">ID do link</span><span class="sxs-lookup"><span data-stu-id="c7b87-224">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c7b87-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c7b87-225">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c7b87-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="c7b87-226">System-Only</span></span>            | <span data-ttu-id="c7b87-227">Falso</span><span class="sxs-lookup"><span data-stu-id="c7b87-227">False</span></span>                                                        |
| <span data-ttu-id="c7b87-228">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c7b87-228">Is-Single-Valued</span></span>       | <span data-ttu-id="c7b87-229">Falso</span><span class="sxs-lookup"><span data-stu-id="c7b87-229">False</span></span>                                                        |
| <span data-ttu-id="c7b87-230">É indexado</span><span class="sxs-lookup"><span data-stu-id="c7b87-230">Is Indexed</span></span>             | <span data-ttu-id="c7b87-231">Falso</span><span class="sxs-lookup"><span data-stu-id="c7b87-231">False</span></span>                                                        |
| <span data-ttu-id="c7b87-232">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c7b87-232">In Global Catalog</span></span>      | <span data-ttu-id="c7b87-233">True</span><span class="sxs-lookup"><span data-stu-id="c7b87-233">True</span></span>                                                         |
| <span data-ttu-id="c7b87-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c7b87-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="c7b87-235">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c7b87-235">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="c7b87-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c7b87-236">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="c7b87-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c7b87-237">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="c7b87-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c7b87-238">Search-Flags</span></span>           | <span data-ttu-id="c7b87-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c7b87-239">0x00000000</span></span>                                                   |
| <span data-ttu-id="c7b87-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c7b87-240">System-Flags</span></span>           | <span data-ttu-id="c7b87-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c7b87-241">0x00000010</span></span>                                                   |
| <span data-ttu-id="c7b87-242">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c7b87-242">Classes used in</span></span>        | [<span data-ttu-id="c7b87-243">**Configuração do MSMQ**</span><span class="sxs-lookup"><span data-stu-id="c7b87-243">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c7b87-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c7b87-244">Windows Server 2012</span></span>



| <span data-ttu-id="c7b87-245">Entrada</span><span class="sxs-lookup"><span data-stu-id="c7b87-245">Entry</span></span> | <span data-ttu-id="c7b87-246">Valor</span><span class="sxs-lookup"><span data-stu-id="c7b87-246">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="c7b87-247">ID do link</span><span class="sxs-lookup"><span data-stu-id="c7b87-247">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c7b87-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c7b87-248">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c7b87-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="c7b87-249">System-Only</span></span>            | <span data-ttu-id="c7b87-250">Falso</span><span class="sxs-lookup"><span data-stu-id="c7b87-250">False</span></span>                                                        |
| <span data-ttu-id="c7b87-251">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c7b87-251">Is-Single-Valued</span></span>       | <span data-ttu-id="c7b87-252">Falso</span><span class="sxs-lookup"><span data-stu-id="c7b87-252">False</span></span>                                                        |
| <span data-ttu-id="c7b87-253">É indexado</span><span class="sxs-lookup"><span data-stu-id="c7b87-253">Is Indexed</span></span>             | <span data-ttu-id="c7b87-254">Falso</span><span class="sxs-lookup"><span data-stu-id="c7b87-254">False</span></span>                                                        |
| <span data-ttu-id="c7b87-255">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c7b87-255">In Global Catalog</span></span>      | <span data-ttu-id="c7b87-256">True</span><span class="sxs-lookup"><span data-stu-id="c7b87-256">True</span></span>                                                         |
| <span data-ttu-id="c7b87-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c7b87-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="c7b87-258">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c7b87-258">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="c7b87-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c7b87-259">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="c7b87-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c7b87-260">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="c7b87-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c7b87-261">Search-Flags</span></span>           | <span data-ttu-id="c7b87-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c7b87-262">0x00000000</span></span>                                                   |
| <span data-ttu-id="c7b87-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c7b87-263">System-Flags</span></span>           | <span data-ttu-id="c7b87-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c7b87-264">0x00000010</span></span>                                                   |
| <span data-ttu-id="c7b87-265">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c7b87-265">Classes used in</span></span>        | [<span data-ttu-id="c7b87-266">**Configuração do MSMQ**</span><span class="sxs-lookup"><span data-stu-id="c7b87-266">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



 

 





