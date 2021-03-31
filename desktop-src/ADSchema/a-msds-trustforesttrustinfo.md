---
title: atributo ms-DS-Trust-Forest-Trust-info
description: Contém informações de confiança de floresta (um BLOB binário) que é usada pelo sistema para um objeto Trusted-Domain.
ms.assetid: 60944ff6-d2b1-4f53-8557-7d79a7d9df51
ms.tgt_platform: multiple
keywords:
- atributo ms-DS-Trust-Forest-Trust-info do AD Schema
- atributo msDS-TrustForestTrustInfo do AD Schema
topic_type:
- apiref
api_name:
- ms-DS-Trust-Forest-Trust-Info
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e259abaeae4d99b80b8ff6a390901f1c9f51e6a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645444"
---
# <a name="ms-ds-trust-forest-trust-info-attribute"></a><span data-ttu-id="18485-105">atributo ms-DS-Trust-Forest-Trust-info</span><span class="sxs-lookup"><span data-stu-id="18485-105">ms-DS-Trust-Forest-Trust-Info attribute</span></span>

<span data-ttu-id="18485-106">Contém informações de confiança de floresta (um BLOB binário) que é usada pelo sistema para um objeto Trusted-Domain.</span><span class="sxs-lookup"><span data-stu-id="18485-106">Contains forest trust information (a binary BLOB) that is used by the system for a Trusted-Domain object.</span></span>



| <span data-ttu-id="18485-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="18485-107">Entry</span></span> | <span data-ttu-id="18485-108">Valor</span><span class="sxs-lookup"><span data-stu-id="18485-108">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18485-109">CN</span><span class="sxs-lookup"><span data-stu-id="18485-109">CN</span></span>                | <span data-ttu-id="18485-110">ms-DS-Trust-Forest-Trust-info</span><span class="sxs-lookup"><span data-stu-id="18485-110">ms-DS-Trust-Forest-Trust-Info</span></span>                                                                                      |
| <span data-ttu-id="18485-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="18485-111">Ldap-Display-Name</span></span> | <span data-ttu-id="18485-112">msDS-TrustForestTrustInfo</span><span class="sxs-lookup"><span data-stu-id="18485-112">msDS-TrustForestTrustInfo</span></span>                                                                                          |
| <span data-ttu-id="18485-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="18485-113">Size</span></span>              | \-                                                                                                                 |
| <span data-ttu-id="18485-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="18485-114">Update Privilege</span></span>  | \-                                                                                                                 |
| <span data-ttu-id="18485-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="18485-115">Update Frequency</span></span>  | <span data-ttu-id="18485-116">Somente quando a relação de confiança entre as florestas é alterada.</span><span class="sxs-lookup"><span data-stu-id="18485-116">Only when trust relationship between forests changes.</span></span> <span data-ttu-id="18485-117">Isso pode acontecer se a topologia de uma floresta confiável for alterada.</span><span class="sxs-lookup"><span data-stu-id="18485-117">This can happen if the topology of a trusted forest changes.</span></span> |
| <span data-ttu-id="18485-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="18485-118">Attribute-Id</span></span>      | <span data-ttu-id="18485-119">1.2.840.113556.1.4.1702</span><span class="sxs-lookup"><span data-stu-id="18485-119">1.2.840.113556.1.4.1702</span></span>                                                                                            |
| <span data-ttu-id="18485-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="18485-120">System-Id-Guid</span></span>    | <span data-ttu-id="18485-121">29cc866e-49d3-4969-942e-1dbc0925d183</span><span class="sxs-lookup"><span data-stu-id="18485-121">29cc866e-49d3-4969-942e-1dbc0925d183</span></span>                                                                               |
| <span data-ttu-id="18485-122">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="18485-122">Syntax</span></span>            | [<span data-ttu-id="18485-123">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="18485-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="18485-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="18485-124">Implementations</span></span>

-   [<span data-ttu-id="18485-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="18485-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="18485-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="18485-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="18485-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="18485-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="18485-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="18485-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="18485-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="18485-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="18485-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="18485-130">Windows Server 2003</span></span>



| <span data-ttu-id="18485-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="18485-131">Entry</span></span> | <span data-ttu-id="18485-132">Valor</span><span class="sxs-lookup"><span data-stu-id="18485-132">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="18485-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="18485-133">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="18485-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18485-134">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="18485-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="18485-135">System-Only</span></span>            | <span data-ttu-id="18485-136">Falso</span><span class="sxs-lookup"><span data-stu-id="18485-136">False</span></span>                                                |
| <span data-ttu-id="18485-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="18485-137">Is-Single-Valued</span></span>       | <span data-ttu-id="18485-138">True</span><span class="sxs-lookup"><span data-stu-id="18485-138">True</span></span>                                                 |
| <span data-ttu-id="18485-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="18485-139">Is Indexed</span></span>             | <span data-ttu-id="18485-140">Falso</span><span class="sxs-lookup"><span data-stu-id="18485-140">False</span></span>                                                |
| <span data-ttu-id="18485-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="18485-141">In Global Catalog</span></span>      | <span data-ttu-id="18485-142">True</span><span class="sxs-lookup"><span data-stu-id="18485-142">True</span></span>                                                 |
| <span data-ttu-id="18485-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="18485-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="18485-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="18485-144">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="18485-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18485-145">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="18485-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18485-146">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="18485-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18485-147">Search-Flags</span></span>           | <span data-ttu-id="18485-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18485-148">0x00000000</span></span>                                           |
| <span data-ttu-id="18485-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18485-149">System-Flags</span></span>           | <span data-ttu-id="18485-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18485-150">0x00000010</span></span>                                           |
| <span data-ttu-id="18485-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="18485-151">Classes used in</span></span>        | [<span data-ttu-id="18485-152">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="18485-152">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="18485-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="18485-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="18485-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="18485-154">Entry</span></span> | <span data-ttu-id="18485-155">Valor</span><span class="sxs-lookup"><span data-stu-id="18485-155">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="18485-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="18485-156">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="18485-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18485-157">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="18485-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="18485-158">System-Only</span></span>            | <span data-ttu-id="18485-159">Falso</span><span class="sxs-lookup"><span data-stu-id="18485-159">False</span></span>                                                |
| <span data-ttu-id="18485-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="18485-160">Is-Single-Valued</span></span>       | <span data-ttu-id="18485-161">True</span><span class="sxs-lookup"><span data-stu-id="18485-161">True</span></span>                                                 |
| <span data-ttu-id="18485-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="18485-162">Is Indexed</span></span>             | <span data-ttu-id="18485-163">Falso</span><span class="sxs-lookup"><span data-stu-id="18485-163">False</span></span>                                                |
| <span data-ttu-id="18485-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="18485-164">In Global Catalog</span></span>      | <span data-ttu-id="18485-165">True</span><span class="sxs-lookup"><span data-stu-id="18485-165">True</span></span>                                                 |
| <span data-ttu-id="18485-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="18485-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="18485-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="18485-167">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="18485-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18485-168">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="18485-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18485-169">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="18485-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18485-170">Search-Flags</span></span>           | <span data-ttu-id="18485-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18485-171">0x00000000</span></span>                                           |
| <span data-ttu-id="18485-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18485-172">System-Flags</span></span>           | <span data-ttu-id="18485-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18485-173">0x00000010</span></span>                                           |
| <span data-ttu-id="18485-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="18485-174">Classes used in</span></span>        | [<span data-ttu-id="18485-175">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="18485-175">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="18485-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18485-176">Windows Server 2008</span></span>



| <span data-ttu-id="18485-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="18485-177">Entry</span></span> | <span data-ttu-id="18485-178">Valor</span><span class="sxs-lookup"><span data-stu-id="18485-178">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="18485-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="18485-179">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="18485-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18485-180">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="18485-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="18485-181">System-Only</span></span>            | <span data-ttu-id="18485-182">Falso</span><span class="sxs-lookup"><span data-stu-id="18485-182">False</span></span>                                                |
| <span data-ttu-id="18485-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="18485-183">Is-Single-Valued</span></span>       | <span data-ttu-id="18485-184">True</span><span class="sxs-lookup"><span data-stu-id="18485-184">True</span></span>                                                 |
| <span data-ttu-id="18485-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="18485-185">Is Indexed</span></span>             | <span data-ttu-id="18485-186">Falso</span><span class="sxs-lookup"><span data-stu-id="18485-186">False</span></span>                                                |
| <span data-ttu-id="18485-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="18485-187">In Global Catalog</span></span>      | <span data-ttu-id="18485-188">True</span><span class="sxs-lookup"><span data-stu-id="18485-188">True</span></span>                                                 |
| <span data-ttu-id="18485-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="18485-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="18485-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="18485-190">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="18485-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18485-191">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="18485-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18485-192">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="18485-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18485-193">Search-Flags</span></span>           | <span data-ttu-id="18485-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18485-194">0x00000000</span></span>                                           |
| <span data-ttu-id="18485-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18485-195">System-Flags</span></span>           | <span data-ttu-id="18485-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18485-196">0x00000010</span></span>                                           |
| <span data-ttu-id="18485-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="18485-197">Classes used in</span></span>        | [<span data-ttu-id="18485-198">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="18485-198">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="18485-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="18485-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="18485-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="18485-200">Entry</span></span> | <span data-ttu-id="18485-201">Valor</span><span class="sxs-lookup"><span data-stu-id="18485-201">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="18485-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="18485-202">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="18485-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18485-203">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="18485-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="18485-204">System-Only</span></span>            | <span data-ttu-id="18485-205">Falso</span><span class="sxs-lookup"><span data-stu-id="18485-205">False</span></span>                                                |
| <span data-ttu-id="18485-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="18485-206">Is-Single-Valued</span></span>       | <span data-ttu-id="18485-207">True</span><span class="sxs-lookup"><span data-stu-id="18485-207">True</span></span>                                                 |
| <span data-ttu-id="18485-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="18485-208">Is Indexed</span></span>             | <span data-ttu-id="18485-209">Falso</span><span class="sxs-lookup"><span data-stu-id="18485-209">False</span></span>                                                |
| <span data-ttu-id="18485-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="18485-210">In Global Catalog</span></span>      | <span data-ttu-id="18485-211">True</span><span class="sxs-lookup"><span data-stu-id="18485-211">True</span></span>                                                 |
| <span data-ttu-id="18485-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="18485-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="18485-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="18485-213">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="18485-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18485-214">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="18485-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18485-215">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="18485-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18485-216">Search-Flags</span></span>           | <span data-ttu-id="18485-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18485-217">0x00000000</span></span>                                           |
| <span data-ttu-id="18485-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18485-218">System-Flags</span></span>           | <span data-ttu-id="18485-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18485-219">0x00000010</span></span>                                           |
| <span data-ttu-id="18485-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="18485-220">Classes used in</span></span>        | [<span data-ttu-id="18485-221">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="18485-221">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="18485-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="18485-222">Windows Server 2012</span></span>



| <span data-ttu-id="18485-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="18485-223">Entry</span></span> | <span data-ttu-id="18485-224">Valor</span><span class="sxs-lookup"><span data-stu-id="18485-224">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="18485-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="18485-225">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="18485-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18485-226">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="18485-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="18485-227">System-Only</span></span>            | <span data-ttu-id="18485-228">Falso</span><span class="sxs-lookup"><span data-stu-id="18485-228">False</span></span>                                                |
| <span data-ttu-id="18485-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="18485-229">Is-Single-Valued</span></span>       | <span data-ttu-id="18485-230">True</span><span class="sxs-lookup"><span data-stu-id="18485-230">True</span></span>                                                 |
| <span data-ttu-id="18485-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="18485-231">Is Indexed</span></span>             | <span data-ttu-id="18485-232">Falso</span><span class="sxs-lookup"><span data-stu-id="18485-232">False</span></span>                                                |
| <span data-ttu-id="18485-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="18485-233">In Global Catalog</span></span>      | <span data-ttu-id="18485-234">True</span><span class="sxs-lookup"><span data-stu-id="18485-234">True</span></span>                                                 |
| <span data-ttu-id="18485-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="18485-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="18485-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="18485-236">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="18485-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18485-237">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="18485-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18485-238">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="18485-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18485-239">Search-Flags</span></span>           | <span data-ttu-id="18485-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18485-240">0x00000000</span></span>                                           |
| <span data-ttu-id="18485-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18485-241">System-Flags</span></span>           | <span data-ttu-id="18485-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18485-242">0x00000010</span></span>                                           |
| <span data-ttu-id="18485-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="18485-243">Classes used in</span></span>        | [<span data-ttu-id="18485-244">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="18485-244">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





