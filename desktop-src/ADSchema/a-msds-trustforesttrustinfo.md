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
# <a name="ms-ds-trust-forest-trust-info-attribute"></a><span data-ttu-id="28419-105">atributo ms-DS-Trust-Forest-Trust-info</span><span class="sxs-lookup"><span data-stu-id="28419-105">ms-DS-Trust-Forest-Trust-Info attribute</span></span>

<span data-ttu-id="28419-106">Contém informações de confiança de floresta (um BLOB binário) que é usada pelo sistema para um objeto Trusted-Domain.</span><span class="sxs-lookup"><span data-stu-id="28419-106">Contains forest trust information (a binary BLOB) that is used by the system for a Trusted-Domain object.</span></span>



| <span data-ttu-id="28419-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="28419-107">Entry</span></span> | <span data-ttu-id="28419-108">Valor</span><span class="sxs-lookup"><span data-stu-id="28419-108">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28419-109">CN</span><span class="sxs-lookup"><span data-stu-id="28419-109">CN</span></span>                | <span data-ttu-id="28419-110">ms-DS-Trust-Forest-Trust-info</span><span class="sxs-lookup"><span data-stu-id="28419-110">ms-DS-Trust-Forest-Trust-Info</span></span>                                                                                      |
| <span data-ttu-id="28419-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="28419-111">Ldap-Display-Name</span></span> | <span data-ttu-id="28419-112">msDS-TrustForestTrustInfo</span><span class="sxs-lookup"><span data-stu-id="28419-112">msDS-TrustForestTrustInfo</span></span>                                                                                          |
| <span data-ttu-id="28419-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="28419-113">Size</span></span>              | \-                                                                                                                 |
| <span data-ttu-id="28419-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="28419-114">Update Privilege</span></span>  | \-                                                                                                                 |
| <span data-ttu-id="28419-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="28419-115">Update Frequency</span></span>  | <span data-ttu-id="28419-116">Somente quando a relação de confiança entre as florestas é alterada.</span><span class="sxs-lookup"><span data-stu-id="28419-116">Only when trust relationship between forests changes.</span></span> <span data-ttu-id="28419-117">Isso pode acontecer se a topologia de uma floresta confiável for alterada.</span><span class="sxs-lookup"><span data-stu-id="28419-117">This can happen if the topology of a trusted forest changes.</span></span> |
| <span data-ttu-id="28419-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="28419-118">Attribute-Id</span></span>      | <span data-ttu-id="28419-119">1.2.840.113556.1.4.1702</span><span class="sxs-lookup"><span data-stu-id="28419-119">1.2.840.113556.1.4.1702</span></span>                                                                                            |
| <span data-ttu-id="28419-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="28419-120">System-Id-Guid</span></span>    | <span data-ttu-id="28419-121">29cc866e-49d3-4969-942e-1dbc0925d183</span><span class="sxs-lookup"><span data-stu-id="28419-121">29cc866e-49d3-4969-942e-1dbc0925d183</span></span>                                                                               |
| <span data-ttu-id="28419-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="28419-122">Syntax</span></span>            | [<span data-ttu-id="28419-123">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="28419-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="28419-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="28419-124">Implementations</span></span>

-   [<span data-ttu-id="28419-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="28419-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="28419-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="28419-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="28419-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="28419-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="28419-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="28419-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="28419-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="28419-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="28419-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="28419-130">Windows Server 2003</span></span>



| <span data-ttu-id="28419-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="28419-131">Entry</span></span> | <span data-ttu-id="28419-132">Valor</span><span class="sxs-lookup"><span data-stu-id="28419-132">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="28419-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="28419-133">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="28419-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28419-134">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="28419-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="28419-135">System-Only</span></span>            | <span data-ttu-id="28419-136">Falso</span><span class="sxs-lookup"><span data-stu-id="28419-136">False</span></span>                                                |
| <span data-ttu-id="28419-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="28419-137">Is-Single-Valued</span></span>       | <span data-ttu-id="28419-138">True</span><span class="sxs-lookup"><span data-stu-id="28419-138">True</span></span>                                                 |
| <span data-ttu-id="28419-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="28419-139">Is Indexed</span></span>             | <span data-ttu-id="28419-140">Falso</span><span class="sxs-lookup"><span data-stu-id="28419-140">False</span></span>                                                |
| <span data-ttu-id="28419-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="28419-141">In Global Catalog</span></span>      | <span data-ttu-id="28419-142">True</span><span class="sxs-lookup"><span data-stu-id="28419-142">True</span></span>                                                 |
| <span data-ttu-id="28419-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="28419-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="28419-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="28419-144">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="28419-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28419-145">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="28419-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28419-146">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="28419-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28419-147">Search-Flags</span></span>           | <span data-ttu-id="28419-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28419-148">0x00000000</span></span>                                           |
| <span data-ttu-id="28419-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28419-149">System-Flags</span></span>           | <span data-ttu-id="28419-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28419-150">0x00000010</span></span>                                           |
| <span data-ttu-id="28419-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="28419-151">Classes used in</span></span>        | [<span data-ttu-id="28419-152">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="28419-152">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="28419-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="28419-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="28419-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="28419-154">Entry</span></span> | <span data-ttu-id="28419-155">Valor</span><span class="sxs-lookup"><span data-stu-id="28419-155">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="28419-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="28419-156">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="28419-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28419-157">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="28419-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="28419-158">System-Only</span></span>            | <span data-ttu-id="28419-159">Falso</span><span class="sxs-lookup"><span data-stu-id="28419-159">False</span></span>                                                |
| <span data-ttu-id="28419-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="28419-160">Is-Single-Valued</span></span>       | <span data-ttu-id="28419-161">True</span><span class="sxs-lookup"><span data-stu-id="28419-161">True</span></span>                                                 |
| <span data-ttu-id="28419-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="28419-162">Is Indexed</span></span>             | <span data-ttu-id="28419-163">Falso</span><span class="sxs-lookup"><span data-stu-id="28419-163">False</span></span>                                                |
| <span data-ttu-id="28419-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="28419-164">In Global Catalog</span></span>      | <span data-ttu-id="28419-165">True</span><span class="sxs-lookup"><span data-stu-id="28419-165">True</span></span>                                                 |
| <span data-ttu-id="28419-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="28419-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="28419-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="28419-167">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="28419-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28419-168">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="28419-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28419-169">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="28419-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28419-170">Search-Flags</span></span>           | <span data-ttu-id="28419-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28419-171">0x00000000</span></span>                                           |
| <span data-ttu-id="28419-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28419-172">System-Flags</span></span>           | <span data-ttu-id="28419-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28419-173">0x00000010</span></span>                                           |
| <span data-ttu-id="28419-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="28419-174">Classes used in</span></span>        | [<span data-ttu-id="28419-175">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="28419-175">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="28419-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="28419-176">Windows Server 2008</span></span>



| <span data-ttu-id="28419-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="28419-177">Entry</span></span> | <span data-ttu-id="28419-178">Valor</span><span class="sxs-lookup"><span data-stu-id="28419-178">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="28419-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="28419-179">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="28419-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28419-180">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="28419-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="28419-181">System-Only</span></span>            | <span data-ttu-id="28419-182">Falso</span><span class="sxs-lookup"><span data-stu-id="28419-182">False</span></span>                                                |
| <span data-ttu-id="28419-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="28419-183">Is-Single-Valued</span></span>       | <span data-ttu-id="28419-184">True</span><span class="sxs-lookup"><span data-stu-id="28419-184">True</span></span>                                                 |
| <span data-ttu-id="28419-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="28419-185">Is Indexed</span></span>             | <span data-ttu-id="28419-186">Falso</span><span class="sxs-lookup"><span data-stu-id="28419-186">False</span></span>                                                |
| <span data-ttu-id="28419-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="28419-187">In Global Catalog</span></span>      | <span data-ttu-id="28419-188">True</span><span class="sxs-lookup"><span data-stu-id="28419-188">True</span></span>                                                 |
| <span data-ttu-id="28419-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="28419-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="28419-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="28419-190">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="28419-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28419-191">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="28419-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28419-192">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="28419-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28419-193">Search-Flags</span></span>           | <span data-ttu-id="28419-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28419-194">0x00000000</span></span>                                           |
| <span data-ttu-id="28419-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28419-195">System-Flags</span></span>           | <span data-ttu-id="28419-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28419-196">0x00000010</span></span>                                           |
| <span data-ttu-id="28419-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="28419-197">Classes used in</span></span>        | [<span data-ttu-id="28419-198">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="28419-198">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="28419-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="28419-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="28419-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="28419-200">Entry</span></span> | <span data-ttu-id="28419-201">Valor</span><span class="sxs-lookup"><span data-stu-id="28419-201">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="28419-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="28419-202">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="28419-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28419-203">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="28419-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="28419-204">System-Only</span></span>            | <span data-ttu-id="28419-205">Falso</span><span class="sxs-lookup"><span data-stu-id="28419-205">False</span></span>                                                |
| <span data-ttu-id="28419-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="28419-206">Is-Single-Valued</span></span>       | <span data-ttu-id="28419-207">True</span><span class="sxs-lookup"><span data-stu-id="28419-207">True</span></span>                                                 |
| <span data-ttu-id="28419-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="28419-208">Is Indexed</span></span>             | <span data-ttu-id="28419-209">Falso</span><span class="sxs-lookup"><span data-stu-id="28419-209">False</span></span>                                                |
| <span data-ttu-id="28419-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="28419-210">In Global Catalog</span></span>      | <span data-ttu-id="28419-211">True</span><span class="sxs-lookup"><span data-stu-id="28419-211">True</span></span>                                                 |
| <span data-ttu-id="28419-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="28419-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="28419-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="28419-213">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="28419-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28419-214">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="28419-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28419-215">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="28419-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28419-216">Search-Flags</span></span>           | <span data-ttu-id="28419-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28419-217">0x00000000</span></span>                                           |
| <span data-ttu-id="28419-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28419-218">System-Flags</span></span>           | <span data-ttu-id="28419-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28419-219">0x00000010</span></span>                                           |
| <span data-ttu-id="28419-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="28419-220">Classes used in</span></span>        | [<span data-ttu-id="28419-221">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="28419-221">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="28419-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="28419-222">Windows Server 2012</span></span>



| <span data-ttu-id="28419-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="28419-223">Entry</span></span> | <span data-ttu-id="28419-224">Valor</span><span class="sxs-lookup"><span data-stu-id="28419-224">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="28419-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="28419-225">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="28419-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28419-226">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="28419-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="28419-227">System-Only</span></span>            | <span data-ttu-id="28419-228">Falso</span><span class="sxs-lookup"><span data-stu-id="28419-228">False</span></span>                                                |
| <span data-ttu-id="28419-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="28419-229">Is-Single-Valued</span></span>       | <span data-ttu-id="28419-230">True</span><span class="sxs-lookup"><span data-stu-id="28419-230">True</span></span>                                                 |
| <span data-ttu-id="28419-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="28419-231">Is Indexed</span></span>             | <span data-ttu-id="28419-232">Falso</span><span class="sxs-lookup"><span data-stu-id="28419-232">False</span></span>                                                |
| <span data-ttu-id="28419-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="28419-233">In Global Catalog</span></span>      | <span data-ttu-id="28419-234">True</span><span class="sxs-lookup"><span data-stu-id="28419-234">True</span></span>                                                 |
| <span data-ttu-id="28419-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="28419-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="28419-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="28419-236">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="28419-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28419-237">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="28419-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28419-238">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="28419-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28419-239">Search-Flags</span></span>           | <span data-ttu-id="28419-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28419-240">0x00000000</span></span>                                           |
| <span data-ttu-id="28419-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28419-241">System-Flags</span></span>           | <span data-ttu-id="28419-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28419-242">0x00000010</span></span>                                           |
| <span data-ttu-id="28419-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="28419-243">Classes used in</span></span>        | [<span data-ttu-id="28419-244">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="28419-244">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





