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
# <a name="ms-ds-trust-forest-trust-info-attribute"></a><span data-ttu-id="ff085-105">atributo ms-DS-Trust-Forest-Trust-info</span><span class="sxs-lookup"><span data-stu-id="ff085-105">ms-DS-Trust-Forest-Trust-Info attribute</span></span>

<span data-ttu-id="ff085-106">Contém informações de confiança de floresta (um BLOB binário) que é usada pelo sistema para um objeto Trusted-Domain.</span><span class="sxs-lookup"><span data-stu-id="ff085-106">Contains forest trust information (a binary BLOB) that is used by the system for a Trusted-Domain object.</span></span>



| <span data-ttu-id="ff085-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="ff085-107">Entry</span></span> | <span data-ttu-id="ff085-108">Valor</span><span class="sxs-lookup"><span data-stu-id="ff085-108">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff085-109">CN</span><span class="sxs-lookup"><span data-stu-id="ff085-109">CN</span></span>                | <span data-ttu-id="ff085-110">ms-DS-Trust-Forest-Trust-info</span><span class="sxs-lookup"><span data-stu-id="ff085-110">ms-DS-Trust-Forest-Trust-Info</span></span>                                                                                      |
| <span data-ttu-id="ff085-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="ff085-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ff085-112">msDS-TrustForestTrustInfo</span><span class="sxs-lookup"><span data-stu-id="ff085-112">msDS-TrustForestTrustInfo</span></span>                                                                                          |
| <span data-ttu-id="ff085-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="ff085-113">Size</span></span>              | \-                                                                                                                 |
| <span data-ttu-id="ff085-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="ff085-114">Update Privilege</span></span>  | \-                                                                                                                 |
| <span data-ttu-id="ff085-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="ff085-115">Update Frequency</span></span>  | <span data-ttu-id="ff085-116">Somente quando a relação de confiança entre as florestas é alterada.</span><span class="sxs-lookup"><span data-stu-id="ff085-116">Only when trust relationship between forests changes.</span></span> <span data-ttu-id="ff085-117">Isso pode acontecer se a topologia de uma floresta confiável for alterada.</span><span class="sxs-lookup"><span data-stu-id="ff085-117">This can happen if the topology of a trusted forest changes.</span></span> |
| <span data-ttu-id="ff085-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ff085-118">Attribute-Id</span></span>      | <span data-ttu-id="ff085-119">1.2.840.113556.1.4.1702</span><span class="sxs-lookup"><span data-stu-id="ff085-119">1.2.840.113556.1.4.1702</span></span>                                                                                            |
| <span data-ttu-id="ff085-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="ff085-120">System-Id-Guid</span></span>    | <span data-ttu-id="ff085-121">29cc866e-49d3-4969-942e-1dbc0925d183</span><span class="sxs-lookup"><span data-stu-id="ff085-121">29cc866e-49d3-4969-942e-1dbc0925d183</span></span>                                                                               |
| <span data-ttu-id="ff085-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff085-122">Syntax</span></span>            | [<span data-ttu-id="ff085-123">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="ff085-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="ff085-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="ff085-124">Implementations</span></span>

-   [<span data-ttu-id="ff085-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ff085-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ff085-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ff085-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ff085-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ff085-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ff085-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ff085-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ff085-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ff085-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="ff085-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ff085-130">Windows Server 2003</span></span>



| <span data-ttu-id="ff085-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="ff085-131">Entry</span></span> | <span data-ttu-id="ff085-132">Valor</span><span class="sxs-lookup"><span data-stu-id="ff085-132">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="ff085-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="ff085-133">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ff085-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff085-134">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ff085-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff085-135">System-Only</span></span>            | <span data-ttu-id="ff085-136">Falso</span><span class="sxs-lookup"><span data-stu-id="ff085-136">False</span></span>                                                |
| <span data-ttu-id="ff085-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ff085-137">Is-Single-Valued</span></span>       | <span data-ttu-id="ff085-138">True</span><span class="sxs-lookup"><span data-stu-id="ff085-138">True</span></span>                                                 |
| <span data-ttu-id="ff085-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="ff085-139">Is Indexed</span></span>             | <span data-ttu-id="ff085-140">Falso</span><span class="sxs-lookup"><span data-stu-id="ff085-140">False</span></span>                                                |
| <span data-ttu-id="ff085-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ff085-141">In Global Catalog</span></span>      | <span data-ttu-id="ff085-142">True</span><span class="sxs-lookup"><span data-stu-id="ff085-142">True</span></span>                                                 |
| <span data-ttu-id="ff085-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ff085-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff085-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ff085-144">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="ff085-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff085-145">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="ff085-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff085-146">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="ff085-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff085-147">Search-Flags</span></span>           | <span data-ttu-id="ff085-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff085-148">0x00000000</span></span>                                           |
| <span data-ttu-id="ff085-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff085-149">System-Flags</span></span>           | <span data-ttu-id="ff085-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff085-150">0x00000010</span></span>                                           |
| <span data-ttu-id="ff085-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ff085-151">Classes used in</span></span>        | [<span data-ttu-id="ff085-152">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="ff085-152">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ff085-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ff085-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ff085-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="ff085-154">Entry</span></span> | <span data-ttu-id="ff085-155">Valor</span><span class="sxs-lookup"><span data-stu-id="ff085-155">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="ff085-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="ff085-156">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ff085-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff085-157">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ff085-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff085-158">System-Only</span></span>            | <span data-ttu-id="ff085-159">Falso</span><span class="sxs-lookup"><span data-stu-id="ff085-159">False</span></span>                                                |
| <span data-ttu-id="ff085-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ff085-160">Is-Single-Valued</span></span>       | <span data-ttu-id="ff085-161">True</span><span class="sxs-lookup"><span data-stu-id="ff085-161">True</span></span>                                                 |
| <span data-ttu-id="ff085-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="ff085-162">Is Indexed</span></span>             | <span data-ttu-id="ff085-163">Falso</span><span class="sxs-lookup"><span data-stu-id="ff085-163">False</span></span>                                                |
| <span data-ttu-id="ff085-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ff085-164">In Global Catalog</span></span>      | <span data-ttu-id="ff085-165">True</span><span class="sxs-lookup"><span data-stu-id="ff085-165">True</span></span>                                                 |
| <span data-ttu-id="ff085-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ff085-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff085-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ff085-167">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="ff085-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff085-168">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="ff085-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff085-169">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="ff085-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff085-170">Search-Flags</span></span>           | <span data-ttu-id="ff085-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff085-171">0x00000000</span></span>                                           |
| <span data-ttu-id="ff085-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff085-172">System-Flags</span></span>           | <span data-ttu-id="ff085-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff085-173">0x00000010</span></span>                                           |
| <span data-ttu-id="ff085-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ff085-174">Classes used in</span></span>        | [<span data-ttu-id="ff085-175">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="ff085-175">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ff085-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff085-176">Windows Server 2008</span></span>



| <span data-ttu-id="ff085-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="ff085-177">Entry</span></span> | <span data-ttu-id="ff085-178">Valor</span><span class="sxs-lookup"><span data-stu-id="ff085-178">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="ff085-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="ff085-179">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ff085-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff085-180">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ff085-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff085-181">System-Only</span></span>            | <span data-ttu-id="ff085-182">Falso</span><span class="sxs-lookup"><span data-stu-id="ff085-182">False</span></span>                                                |
| <span data-ttu-id="ff085-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ff085-183">Is-Single-Valued</span></span>       | <span data-ttu-id="ff085-184">True</span><span class="sxs-lookup"><span data-stu-id="ff085-184">True</span></span>                                                 |
| <span data-ttu-id="ff085-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="ff085-185">Is Indexed</span></span>             | <span data-ttu-id="ff085-186">Falso</span><span class="sxs-lookup"><span data-stu-id="ff085-186">False</span></span>                                                |
| <span data-ttu-id="ff085-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ff085-187">In Global Catalog</span></span>      | <span data-ttu-id="ff085-188">True</span><span class="sxs-lookup"><span data-stu-id="ff085-188">True</span></span>                                                 |
| <span data-ttu-id="ff085-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ff085-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff085-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ff085-190">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="ff085-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff085-191">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="ff085-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff085-192">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="ff085-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff085-193">Search-Flags</span></span>           | <span data-ttu-id="ff085-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff085-194">0x00000000</span></span>                                           |
| <span data-ttu-id="ff085-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff085-195">System-Flags</span></span>           | <span data-ttu-id="ff085-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff085-196">0x00000010</span></span>                                           |
| <span data-ttu-id="ff085-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ff085-197">Classes used in</span></span>        | [<span data-ttu-id="ff085-198">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="ff085-198">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ff085-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ff085-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ff085-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="ff085-200">Entry</span></span> | <span data-ttu-id="ff085-201">Valor</span><span class="sxs-lookup"><span data-stu-id="ff085-201">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="ff085-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="ff085-202">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ff085-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff085-203">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ff085-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff085-204">System-Only</span></span>            | <span data-ttu-id="ff085-205">Falso</span><span class="sxs-lookup"><span data-stu-id="ff085-205">False</span></span>                                                |
| <span data-ttu-id="ff085-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ff085-206">Is-Single-Valued</span></span>       | <span data-ttu-id="ff085-207">True</span><span class="sxs-lookup"><span data-stu-id="ff085-207">True</span></span>                                                 |
| <span data-ttu-id="ff085-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="ff085-208">Is Indexed</span></span>             | <span data-ttu-id="ff085-209">Falso</span><span class="sxs-lookup"><span data-stu-id="ff085-209">False</span></span>                                                |
| <span data-ttu-id="ff085-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ff085-210">In Global Catalog</span></span>      | <span data-ttu-id="ff085-211">True</span><span class="sxs-lookup"><span data-stu-id="ff085-211">True</span></span>                                                 |
| <span data-ttu-id="ff085-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ff085-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff085-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ff085-213">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="ff085-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff085-214">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="ff085-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff085-215">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="ff085-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff085-216">Search-Flags</span></span>           | <span data-ttu-id="ff085-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff085-217">0x00000000</span></span>                                           |
| <span data-ttu-id="ff085-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff085-218">System-Flags</span></span>           | <span data-ttu-id="ff085-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff085-219">0x00000010</span></span>                                           |
| <span data-ttu-id="ff085-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ff085-220">Classes used in</span></span>        | [<span data-ttu-id="ff085-221">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="ff085-221">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ff085-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ff085-222">Windows Server 2012</span></span>



| <span data-ttu-id="ff085-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="ff085-223">Entry</span></span> | <span data-ttu-id="ff085-224">Valor</span><span class="sxs-lookup"><span data-stu-id="ff085-224">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="ff085-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="ff085-225">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ff085-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff085-226">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ff085-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff085-227">System-Only</span></span>            | <span data-ttu-id="ff085-228">Falso</span><span class="sxs-lookup"><span data-stu-id="ff085-228">False</span></span>                                                |
| <span data-ttu-id="ff085-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="ff085-229">Is-Single-Valued</span></span>       | <span data-ttu-id="ff085-230">True</span><span class="sxs-lookup"><span data-stu-id="ff085-230">True</span></span>                                                 |
| <span data-ttu-id="ff085-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="ff085-231">Is Indexed</span></span>             | <span data-ttu-id="ff085-232">Falso</span><span class="sxs-lookup"><span data-stu-id="ff085-232">False</span></span>                                                |
| <span data-ttu-id="ff085-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="ff085-233">In Global Catalog</span></span>      | <span data-ttu-id="ff085-234">True</span><span class="sxs-lookup"><span data-stu-id="ff085-234">True</span></span>                                                 |
| <span data-ttu-id="ff085-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="ff085-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff085-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="ff085-236">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="ff085-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff085-237">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="ff085-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff085-238">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="ff085-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff085-239">Search-Flags</span></span>           | <span data-ttu-id="ff085-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ff085-240">0x00000000</span></span>                                           |
| <span data-ttu-id="ff085-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff085-241">System-Flags</span></span>           | <span data-ttu-id="ff085-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff085-242">0x00000010</span></span>                                           |
| <span data-ttu-id="ff085-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="ff085-243">Classes used in</span></span>        | [<span data-ttu-id="ff085-244">**Domínio confiável**</span><span class="sxs-lookup"><span data-stu-id="ff085-244">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





