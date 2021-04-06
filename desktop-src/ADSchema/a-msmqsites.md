---
title: MSMQ-Sites atributo
description: A lista de sites aos quais o computador pertence (uma matriz de objectGUIDs de sites, geralmente não mais de um GUID).
ms.assetid: 0f6cfc3a-9edb-4291-a5df-06c0f1a6add8
ms.tgt_platform: multiple
keywords:
- Esquema de MSMQ-Sites do atributo AD
- Esquema de AD do atributo mSMQSites
topic_type:
- apiref
api_name:
- MSMQ-Sites
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47512a20301f3b1dca96c86efe604b0eacc4a73e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103919601"
---
# <a name="msmq-sites-attribute"></a><span data-ttu-id="ad6c7-105">MSMQ-Sites atributo</span><span class="sxs-lookup"><span data-stu-id="ad6c7-105">MSMQ-Sites attribute</span></span>

<span data-ttu-id="ad6c7-106">A lista de sites aos quais o computador pertence (uma matriz de objectGUIDs de sites, geralmente não mais de um GUID).</span><span class="sxs-lookup"><span data-stu-id="ad6c7-106">The list of sites that the computer belongs to (an array of the sites' objectGUIDs, usually not more than one GUID).</span></span>



| <span data-ttu-id="ad6c7-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="ad6c7-107">Entry</span></span> | <span data-ttu-id="ad6c7-108">Valor</span><span class="sxs-lookup"><span data-stu-id="ad6c7-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="ad6c7-109">CN</span><span class="sxs-lookup"><span data-stu-id="ad6c7-109">CN</span></span>                | <span data-ttu-id="ad6c7-110">MSMQ-Sites</span><span class="sxs-lookup"><span data-stu-id="ad6c7-110">MSMQ-Sites</span></span>                                            |
| <span data-ttu-id="ad6c7-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ad6c7-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ad6c7-112">mSMQSites</span><span class="sxs-lookup"><span data-stu-id="ad6c7-112">mSMQSites</span></span>                                             |
| <span data-ttu-id="ad6c7-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="ad6c7-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="ad6c7-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="ad6c7-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="ad6c7-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="ad6c7-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="ad6c7-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ad6c7-116">Attribute-Id</span></span>      | <span data-ttu-id="ad6c7-117">1.2.840.113556.1.4.927</span><span class="sxs-lookup"><span data-stu-id="ad6c7-117">1.2.840.113556.1.4.927</span></span>                                |
| <span data-ttu-id="ad6c7-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ad6c7-118">System-Id-Guid</span></span>    | <span data-ttu-id="ad6c7-119">9a0dc32a-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="ad6c7-119">9a0dc32a-c100-11d1-bbc5-0080c76670c0</span></span>                  |
| <span data-ttu-id="ad6c7-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad6c7-120">Syntax</span></span>            | [<span data-ttu-id="ad6c7-121">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="ad6c7-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="ad6c7-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="ad6c7-122">Implementations</span></span>

-   [<span data-ttu-id="ad6c7-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ad6c7-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ad6c7-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ad6c7-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ad6c7-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ad6c7-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ad6c7-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ad6c7-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ad6c7-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ad6c7-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ad6c7-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ad6c7-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ad6c7-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ad6c7-129">Windows 2000 Server</span></span>



| <span data-ttu-id="ad6c7-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="ad6c7-130">Entry</span></span> | <span data-ttu-id="ad6c7-131">Valor</span><span class="sxs-lookup"><span data-stu-id="ad6c7-131">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="ad6c7-132">ID do link</span><span class="sxs-lookup"><span data-stu-id="ad6c7-132">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="ad6c7-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad6c7-133">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="ad6c7-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad6c7-134">System-Only</span></span>            | <span data-ttu-id="ad6c7-135">Falso</span><span class="sxs-lookup"><span data-stu-id="ad6c7-135">False</span></span>                                                        |
| <span data-ttu-id="ad6c7-136">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ad6c7-136">Is-Single-Valued</span></span>       | <span data-ttu-id="ad6c7-137">Falso</span><span class="sxs-lookup"><span data-stu-id="ad6c7-137">False</span></span>                                                        |
| <span data-ttu-id="ad6c7-138">É indexado</span><span class="sxs-lookup"><span data-stu-id="ad6c7-138">Is Indexed</span></span>             | <span data-ttu-id="ad6c7-139">Falso</span><span class="sxs-lookup"><span data-stu-id="ad6c7-139">False</span></span>                                                        |
| <span data-ttu-id="ad6c7-140">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ad6c7-140">In Global Catalog</span></span>      | <span data-ttu-id="ad6c7-141">True</span><span class="sxs-lookup"><span data-stu-id="ad6c7-141">True</span></span>                                                         |
| <span data-ttu-id="ad6c7-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ad6c7-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad6c7-143">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ad6c7-143">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="ad6c7-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad6c7-144">Range-Lower</span></span>            | <span data-ttu-id="ad6c7-145">16</span><span class="sxs-lookup"><span data-stu-id="ad6c7-145">16</span></span>                                                           |
| <span data-ttu-id="ad6c7-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad6c7-146">Range-Upper</span></span>            | <span data-ttu-id="ad6c7-147">16</span><span class="sxs-lookup"><span data-stu-id="ad6c7-147">16</span></span>                                                           |
| <span data-ttu-id="ad6c7-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad6c7-148">Search-Flags</span></span>           | <span data-ttu-id="ad6c7-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad6c7-149">0x00000000</span></span>                                                   |
| <span data-ttu-id="ad6c7-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad6c7-150">System-Flags</span></span>           | <span data-ttu-id="ad6c7-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ad6c7-151">0x00000010</span></span>                                                   |
| <span data-ttu-id="ad6c7-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ad6c7-152">Classes used in</span></span>        | [<span data-ttu-id="ad6c7-153">**Configuração do MSMQ**</span><span class="sxs-lookup"><span data-stu-id="ad6c7-153">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ad6c7-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ad6c7-154">Windows Server 2003</span></span>



| <span data-ttu-id="ad6c7-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="ad6c7-155">Entry</span></span> | <span data-ttu-id="ad6c7-156">Valor</span><span class="sxs-lookup"><span data-stu-id="ad6c7-156">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="ad6c7-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="ad6c7-157">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="ad6c7-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad6c7-158">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="ad6c7-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad6c7-159">System-Only</span></span>            | <span data-ttu-id="ad6c7-160">Falso</span><span class="sxs-lookup"><span data-stu-id="ad6c7-160">False</span></span>                                                        |
| <span data-ttu-id="ad6c7-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ad6c7-161">Is-Single-Valued</span></span>       | <span data-ttu-id="ad6c7-162">Falso</span><span class="sxs-lookup"><span data-stu-id="ad6c7-162">False</span></span>                                                        |
| <span data-ttu-id="ad6c7-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="ad6c7-163">Is Indexed</span></span>             | <span data-ttu-id="ad6c7-164">Falso</span><span class="sxs-lookup"><span data-stu-id="ad6c7-164">False</span></span>                                                        |
| <span data-ttu-id="ad6c7-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ad6c7-165">In Global Catalog</span></span>      | <span data-ttu-id="ad6c7-166">True</span><span class="sxs-lookup"><span data-stu-id="ad6c7-166">True</span></span>                                                         |
| <span data-ttu-id="ad6c7-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ad6c7-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad6c7-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ad6c7-168">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="ad6c7-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad6c7-169">Range-Lower</span></span>            | <span data-ttu-id="ad6c7-170">16</span><span class="sxs-lookup"><span data-stu-id="ad6c7-170">16</span></span>                                                           |
| <span data-ttu-id="ad6c7-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad6c7-171">Range-Upper</span></span>            | <span data-ttu-id="ad6c7-172">16</span><span class="sxs-lookup"><span data-stu-id="ad6c7-172">16</span></span>                                                           |
| <span data-ttu-id="ad6c7-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad6c7-173">Search-Flags</span></span>           | <span data-ttu-id="ad6c7-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad6c7-174">0x00000000</span></span>                                                   |
| <span data-ttu-id="ad6c7-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad6c7-175">System-Flags</span></span>           | <span data-ttu-id="ad6c7-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ad6c7-176">0x00000010</span></span>                                                   |
| <span data-ttu-id="ad6c7-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ad6c7-177">Classes used in</span></span>        | [<span data-ttu-id="ad6c7-178">**Configuração do MSMQ**</span><span class="sxs-lookup"><span data-stu-id="ad6c7-178">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ad6c7-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ad6c7-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ad6c7-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="ad6c7-180">Entry</span></span> | <span data-ttu-id="ad6c7-181">Valor</span><span class="sxs-lookup"><span data-stu-id="ad6c7-181">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="ad6c7-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="ad6c7-182">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="ad6c7-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad6c7-183">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="ad6c7-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad6c7-184">System-Only</span></span>            | <span data-ttu-id="ad6c7-185">Falso</span><span class="sxs-lookup"><span data-stu-id="ad6c7-185">False</span></span>                                                        |
| <span data-ttu-id="ad6c7-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ad6c7-186">Is-Single-Valued</span></span>       | <span data-ttu-id="ad6c7-187">Falso</span><span class="sxs-lookup"><span data-stu-id="ad6c7-187">False</span></span>                                                        |
| <span data-ttu-id="ad6c7-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="ad6c7-188">Is Indexed</span></span>             | <span data-ttu-id="ad6c7-189">Falso</span><span class="sxs-lookup"><span data-stu-id="ad6c7-189">False</span></span>                                                        |
| <span data-ttu-id="ad6c7-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ad6c7-190">In Global Catalog</span></span>      | <span data-ttu-id="ad6c7-191">True</span><span class="sxs-lookup"><span data-stu-id="ad6c7-191">True</span></span>                                                         |
| <span data-ttu-id="ad6c7-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ad6c7-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad6c7-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ad6c7-193">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="ad6c7-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad6c7-194">Range-Lower</span></span>            | <span data-ttu-id="ad6c7-195">16</span><span class="sxs-lookup"><span data-stu-id="ad6c7-195">16</span></span>                                                           |
| <span data-ttu-id="ad6c7-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad6c7-196">Range-Upper</span></span>            | <span data-ttu-id="ad6c7-197">16</span><span class="sxs-lookup"><span data-stu-id="ad6c7-197">16</span></span>                                                           |
| <span data-ttu-id="ad6c7-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad6c7-198">Search-Flags</span></span>           | <span data-ttu-id="ad6c7-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad6c7-199">0x00000000</span></span>                                                   |
| <span data-ttu-id="ad6c7-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad6c7-200">System-Flags</span></span>           | <span data-ttu-id="ad6c7-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ad6c7-201">0x00000010</span></span>                                                   |
| <span data-ttu-id="ad6c7-202">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ad6c7-202">Classes used in</span></span>        | [<span data-ttu-id="ad6c7-203">**Configuração do MSMQ**</span><span class="sxs-lookup"><span data-stu-id="ad6c7-203">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ad6c7-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad6c7-204">Windows Server 2008</span></span>



| <span data-ttu-id="ad6c7-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="ad6c7-205">Entry</span></span> | <span data-ttu-id="ad6c7-206">Valor</span><span class="sxs-lookup"><span data-stu-id="ad6c7-206">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="ad6c7-207">ID do link</span><span class="sxs-lookup"><span data-stu-id="ad6c7-207">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="ad6c7-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad6c7-208">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="ad6c7-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad6c7-209">System-Only</span></span>            | <span data-ttu-id="ad6c7-210">Falso</span><span class="sxs-lookup"><span data-stu-id="ad6c7-210">False</span></span>                                                        |
| <span data-ttu-id="ad6c7-211">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ad6c7-211">Is-Single-Valued</span></span>       | <span data-ttu-id="ad6c7-212">Falso</span><span class="sxs-lookup"><span data-stu-id="ad6c7-212">False</span></span>                                                        |
| <span data-ttu-id="ad6c7-213">É indexado</span><span class="sxs-lookup"><span data-stu-id="ad6c7-213">Is Indexed</span></span>             | <span data-ttu-id="ad6c7-214">Falso</span><span class="sxs-lookup"><span data-stu-id="ad6c7-214">False</span></span>                                                        |
| <span data-ttu-id="ad6c7-215">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ad6c7-215">In Global Catalog</span></span>      | <span data-ttu-id="ad6c7-216">True</span><span class="sxs-lookup"><span data-stu-id="ad6c7-216">True</span></span>                                                         |
| <span data-ttu-id="ad6c7-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ad6c7-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad6c7-218">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ad6c7-218">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="ad6c7-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad6c7-219">Range-Lower</span></span>            | <span data-ttu-id="ad6c7-220">16</span><span class="sxs-lookup"><span data-stu-id="ad6c7-220">16</span></span>                                                           |
| <span data-ttu-id="ad6c7-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad6c7-221">Range-Upper</span></span>            | <span data-ttu-id="ad6c7-222">16</span><span class="sxs-lookup"><span data-stu-id="ad6c7-222">16</span></span>                                                           |
| <span data-ttu-id="ad6c7-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad6c7-223">Search-Flags</span></span>           | <span data-ttu-id="ad6c7-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad6c7-224">0x00000000</span></span>                                                   |
| <span data-ttu-id="ad6c7-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad6c7-225">System-Flags</span></span>           | <span data-ttu-id="ad6c7-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ad6c7-226">0x00000010</span></span>                                                   |
| <span data-ttu-id="ad6c7-227">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ad6c7-227">Classes used in</span></span>        | [<span data-ttu-id="ad6c7-228">**Configuração do MSMQ**</span><span class="sxs-lookup"><span data-stu-id="ad6c7-228">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ad6c7-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ad6c7-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ad6c7-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="ad6c7-230">Entry</span></span> | <span data-ttu-id="ad6c7-231">Valor</span><span class="sxs-lookup"><span data-stu-id="ad6c7-231">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="ad6c7-232">ID do link</span><span class="sxs-lookup"><span data-stu-id="ad6c7-232">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="ad6c7-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad6c7-233">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="ad6c7-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad6c7-234">System-Only</span></span>            | <span data-ttu-id="ad6c7-235">Falso</span><span class="sxs-lookup"><span data-stu-id="ad6c7-235">False</span></span>                                                        |
| <span data-ttu-id="ad6c7-236">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ad6c7-236">Is-Single-Valued</span></span>       | <span data-ttu-id="ad6c7-237">Falso</span><span class="sxs-lookup"><span data-stu-id="ad6c7-237">False</span></span>                                                        |
| <span data-ttu-id="ad6c7-238">É indexado</span><span class="sxs-lookup"><span data-stu-id="ad6c7-238">Is Indexed</span></span>             | <span data-ttu-id="ad6c7-239">Falso</span><span class="sxs-lookup"><span data-stu-id="ad6c7-239">False</span></span>                                                        |
| <span data-ttu-id="ad6c7-240">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ad6c7-240">In Global Catalog</span></span>      | <span data-ttu-id="ad6c7-241">True</span><span class="sxs-lookup"><span data-stu-id="ad6c7-241">True</span></span>                                                         |
| <span data-ttu-id="ad6c7-242">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ad6c7-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad6c7-243">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ad6c7-243">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="ad6c7-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad6c7-244">Range-Lower</span></span>            | <span data-ttu-id="ad6c7-245">16</span><span class="sxs-lookup"><span data-stu-id="ad6c7-245">16</span></span>                                                           |
| <span data-ttu-id="ad6c7-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad6c7-246">Range-Upper</span></span>            | <span data-ttu-id="ad6c7-247">16</span><span class="sxs-lookup"><span data-stu-id="ad6c7-247">16</span></span>                                                           |
| <span data-ttu-id="ad6c7-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad6c7-248">Search-Flags</span></span>           | <span data-ttu-id="ad6c7-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad6c7-249">0x00000000</span></span>                                                   |
| <span data-ttu-id="ad6c7-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad6c7-250">System-Flags</span></span>           | <span data-ttu-id="ad6c7-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ad6c7-251">0x00000010</span></span>                                                   |
| <span data-ttu-id="ad6c7-252">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ad6c7-252">Classes used in</span></span>        | [<span data-ttu-id="ad6c7-253">**Configuração do MSMQ**</span><span class="sxs-lookup"><span data-stu-id="ad6c7-253">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ad6c7-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ad6c7-254">Windows Server 2012</span></span>



| <span data-ttu-id="ad6c7-255">Entrada</span><span class="sxs-lookup"><span data-stu-id="ad6c7-255">Entry</span></span> | <span data-ttu-id="ad6c7-256">Valor</span><span class="sxs-lookup"><span data-stu-id="ad6c7-256">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="ad6c7-257">ID do link</span><span class="sxs-lookup"><span data-stu-id="ad6c7-257">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="ad6c7-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad6c7-258">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="ad6c7-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad6c7-259">System-Only</span></span>            | <span data-ttu-id="ad6c7-260">Falso</span><span class="sxs-lookup"><span data-stu-id="ad6c7-260">False</span></span>                                                        |
| <span data-ttu-id="ad6c7-261">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ad6c7-261">Is-Single-Valued</span></span>       | <span data-ttu-id="ad6c7-262">Falso</span><span class="sxs-lookup"><span data-stu-id="ad6c7-262">False</span></span>                                                        |
| <span data-ttu-id="ad6c7-263">É indexado</span><span class="sxs-lookup"><span data-stu-id="ad6c7-263">Is Indexed</span></span>             | <span data-ttu-id="ad6c7-264">Falso</span><span class="sxs-lookup"><span data-stu-id="ad6c7-264">False</span></span>                                                        |
| <span data-ttu-id="ad6c7-265">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ad6c7-265">In Global Catalog</span></span>      | <span data-ttu-id="ad6c7-266">True</span><span class="sxs-lookup"><span data-stu-id="ad6c7-266">True</span></span>                                                         |
| <span data-ttu-id="ad6c7-267">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ad6c7-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad6c7-268">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ad6c7-268">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="ad6c7-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad6c7-269">Range-Lower</span></span>            | <span data-ttu-id="ad6c7-270">16</span><span class="sxs-lookup"><span data-stu-id="ad6c7-270">16</span></span>                                                           |
| <span data-ttu-id="ad6c7-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad6c7-271">Range-Upper</span></span>            | <span data-ttu-id="ad6c7-272">16</span><span class="sxs-lookup"><span data-stu-id="ad6c7-272">16</span></span>                                                           |
| <span data-ttu-id="ad6c7-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad6c7-273">Search-Flags</span></span>           | <span data-ttu-id="ad6c7-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad6c7-274">0x00000000</span></span>                                                   |
| <span data-ttu-id="ad6c7-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad6c7-275">System-Flags</span></span>           | <span data-ttu-id="ad6c7-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ad6c7-276">0x00000010</span></span>                                                   |
| <span data-ttu-id="ad6c7-277">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ad6c7-277">Classes used in</span></span>        | [<span data-ttu-id="ad6c7-278">**Configuração do MSMQ**</span><span class="sxs-lookup"><span data-stu-id="ad6c7-278">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



 

 





