---
title: MS-DS-per-user-Trust-preparações-atributo de cota
description: Usado para impor uma cota por usuário para excluir Trusted-Domain objetos quando a autorização é baseada na correspondência do SID do usuário.
ms.assetid: 4db98754-a2d1-43a4-b9cb-0e3fcbbf3ed9
ms.tgt_platform: multiple
keywords:
- MS-DS-per-user-Trust-preparações-esquema de AD do atributo de cota
- atributo msDS-PerUserTrustTombstonesQuota do AD Schema
topic_type:
- apiref
api_name:
- MS-DS-Per-User-Trust-Tombstones-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c94bb62b822552a863df99dac83e98462514c42
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105755895"
---
# <a name="ms-ds-per-user-trust-tombstones-quota-attribute"></a><span data-ttu-id="c7846-105">MS-DS-per-user-Trust-preparações-atributo de cota</span><span class="sxs-lookup"><span data-stu-id="c7846-105">MS-DS-Per-User-Trust-Tombstones-Quota attribute</span></span>

<span data-ttu-id="c7846-106">Usado para impor uma cota por usuário para excluir Trusted-Domain objetos quando a autorização é baseada na correspondência do SID do usuário.</span><span class="sxs-lookup"><span data-stu-id="c7846-106">Used to enforce a per-user quota for deleting Trusted-Domain objects when authorization is based on matching the user's SID.</span></span>



| <span data-ttu-id="c7846-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="c7846-107">Entry</span></span> | <span data-ttu-id="c7846-108">Valor</span><span class="sxs-lookup"><span data-stu-id="c7846-108">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="c7846-109">CN</span><span class="sxs-lookup"><span data-stu-id="c7846-109">CN</span></span>                | <span data-ttu-id="c7846-110">MS-DS-per-user-Trust-preparações-cota</span><span class="sxs-lookup"><span data-stu-id="c7846-110">MS-DS-Per-User-Trust-Tombstones-Quota</span></span>     |
| <span data-ttu-id="c7846-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c7846-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c7846-112">msDS-PerUserTrustTombstonesQuota</span><span class="sxs-lookup"><span data-stu-id="c7846-112">msDS-PerUserTrustTombstonesQuota</span></span>          |
| <span data-ttu-id="c7846-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="c7846-113">Size</span></span>              | \-                                        |
| <span data-ttu-id="c7846-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="c7846-114">Update Privilege</span></span>  | <span data-ttu-id="c7846-115">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="c7846-115">Domain administrator</span></span>                      |
| <span data-ttu-id="c7846-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="c7846-116">Update Frequency</span></span>  | <span data-ttu-id="c7846-117">Na criação da floresta e raramente depois disso.</span><span class="sxs-lookup"><span data-stu-id="c7846-117">At forest creation and rarely after that.</span></span> |
| <span data-ttu-id="c7846-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c7846-118">Attribute-Id</span></span>      | <span data-ttu-id="c7846-119">1.2.840.113556.1.4.1790</span><span class="sxs-lookup"><span data-stu-id="c7846-119">1.2.840.113556.1.4.1790</span></span>                   |
| <span data-ttu-id="c7846-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c7846-120">System-Id-Guid</span></span>    | <span data-ttu-id="c7846-121">8b70a6c6-50f9-4fa3-a71e-1ce03040449b</span><span class="sxs-lookup"><span data-stu-id="c7846-121">8b70a6c6-50f9-4fa3-a71e-1ce03040449b</span></span>      |
| <span data-ttu-id="c7846-122">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c7846-122">Syntax</span></span>            | [<span data-ttu-id="c7846-123">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="c7846-123">**Enumeration**</span></span>](s-enumeration.md)      |



## <a name="implementations"></a><span data-ttu-id="c7846-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="c7846-124">Implementations</span></span>

-   [<span data-ttu-id="c7846-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c7846-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c7846-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c7846-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c7846-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c7846-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c7846-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c7846-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c7846-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c7846-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="c7846-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c7846-130">Windows Server 2003</span></span>



| <span data-ttu-id="c7846-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="c7846-131">Entry</span></span> | <span data-ttu-id="c7846-132">Valor</span><span class="sxs-lookup"><span data-stu-id="c7846-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c7846-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="c7846-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c7846-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c7846-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c7846-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="c7846-135">System-Only</span></span>            | <span data-ttu-id="c7846-136">Falso</span><span class="sxs-lookup"><span data-stu-id="c7846-136">False</span></span>                                        |
| <span data-ttu-id="c7846-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c7846-137">Is-Single-Valued</span></span>       | <span data-ttu-id="c7846-138">True</span><span class="sxs-lookup"><span data-stu-id="c7846-138">True</span></span>                                         |
| <span data-ttu-id="c7846-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="c7846-139">Is Indexed</span></span>             | <span data-ttu-id="c7846-140">Falso</span><span class="sxs-lookup"><span data-stu-id="c7846-140">False</span></span>                                        |
| <span data-ttu-id="c7846-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c7846-141">In Global Catalog</span></span>      | <span data-ttu-id="c7846-142">Falso</span><span class="sxs-lookup"><span data-stu-id="c7846-142">False</span></span>                                        |
| <span data-ttu-id="c7846-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c7846-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="c7846-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c7846-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c7846-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c7846-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c7846-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c7846-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c7846-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c7846-147">Search-Flags</span></span>           | <span data-ttu-id="c7846-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c7846-148">0x00000000</span></span>                                   |
| <span data-ttu-id="c7846-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c7846-149">System-Flags</span></span>           | <span data-ttu-id="c7846-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c7846-150">0x00000010</span></span>                                   |
| <span data-ttu-id="c7846-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c7846-151">Classes used in</span></span>        | [<span data-ttu-id="c7846-152">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="c7846-152">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c7846-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c7846-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c7846-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="c7846-154">Entry</span></span> | <span data-ttu-id="c7846-155">Valor</span><span class="sxs-lookup"><span data-stu-id="c7846-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c7846-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="c7846-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c7846-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c7846-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c7846-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="c7846-158">System-Only</span></span>            | <span data-ttu-id="c7846-159">Falso</span><span class="sxs-lookup"><span data-stu-id="c7846-159">False</span></span>                                        |
| <span data-ttu-id="c7846-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c7846-160">Is-Single-Valued</span></span>       | <span data-ttu-id="c7846-161">True</span><span class="sxs-lookup"><span data-stu-id="c7846-161">True</span></span>                                         |
| <span data-ttu-id="c7846-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="c7846-162">Is Indexed</span></span>             | <span data-ttu-id="c7846-163">Falso</span><span class="sxs-lookup"><span data-stu-id="c7846-163">False</span></span>                                        |
| <span data-ttu-id="c7846-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c7846-164">In Global Catalog</span></span>      | <span data-ttu-id="c7846-165">Falso</span><span class="sxs-lookup"><span data-stu-id="c7846-165">False</span></span>                                        |
| <span data-ttu-id="c7846-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c7846-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="c7846-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c7846-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c7846-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c7846-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c7846-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c7846-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c7846-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c7846-170">Search-Flags</span></span>           | <span data-ttu-id="c7846-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c7846-171">0x00000000</span></span>                                   |
| <span data-ttu-id="c7846-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c7846-172">System-Flags</span></span>           | <span data-ttu-id="c7846-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c7846-173">0x00000010</span></span>                                   |
| <span data-ttu-id="c7846-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c7846-174">Classes used in</span></span>        | [<span data-ttu-id="c7846-175">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="c7846-175">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c7846-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7846-176">Windows Server 2008</span></span>



| <span data-ttu-id="c7846-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="c7846-177">Entry</span></span> | <span data-ttu-id="c7846-178">Valor</span><span class="sxs-lookup"><span data-stu-id="c7846-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c7846-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="c7846-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c7846-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c7846-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c7846-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="c7846-181">System-Only</span></span>            | <span data-ttu-id="c7846-182">Falso</span><span class="sxs-lookup"><span data-stu-id="c7846-182">False</span></span>                                        |
| <span data-ttu-id="c7846-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c7846-183">Is-Single-Valued</span></span>       | <span data-ttu-id="c7846-184">True</span><span class="sxs-lookup"><span data-stu-id="c7846-184">True</span></span>                                         |
| <span data-ttu-id="c7846-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="c7846-185">Is Indexed</span></span>             | <span data-ttu-id="c7846-186">Falso</span><span class="sxs-lookup"><span data-stu-id="c7846-186">False</span></span>                                        |
| <span data-ttu-id="c7846-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c7846-187">In Global Catalog</span></span>      | <span data-ttu-id="c7846-188">Falso</span><span class="sxs-lookup"><span data-stu-id="c7846-188">False</span></span>                                        |
| <span data-ttu-id="c7846-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c7846-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="c7846-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c7846-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c7846-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c7846-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c7846-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c7846-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c7846-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c7846-193">Search-Flags</span></span>           | <span data-ttu-id="c7846-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c7846-194">0x00000000</span></span>                                   |
| <span data-ttu-id="c7846-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c7846-195">System-Flags</span></span>           | <span data-ttu-id="c7846-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c7846-196">0x00000010</span></span>                                   |
| <span data-ttu-id="c7846-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c7846-197">Classes used in</span></span>        | [<span data-ttu-id="c7846-198">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="c7846-198">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c7846-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c7846-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c7846-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="c7846-200">Entry</span></span> | <span data-ttu-id="c7846-201">Valor</span><span class="sxs-lookup"><span data-stu-id="c7846-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c7846-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="c7846-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c7846-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c7846-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c7846-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="c7846-204">System-Only</span></span>            | <span data-ttu-id="c7846-205">Falso</span><span class="sxs-lookup"><span data-stu-id="c7846-205">False</span></span>                                        |
| <span data-ttu-id="c7846-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c7846-206">Is-Single-Valued</span></span>       | <span data-ttu-id="c7846-207">True</span><span class="sxs-lookup"><span data-stu-id="c7846-207">True</span></span>                                         |
| <span data-ttu-id="c7846-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="c7846-208">Is Indexed</span></span>             | <span data-ttu-id="c7846-209">Falso</span><span class="sxs-lookup"><span data-stu-id="c7846-209">False</span></span>                                        |
| <span data-ttu-id="c7846-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c7846-210">In Global Catalog</span></span>      | <span data-ttu-id="c7846-211">Falso</span><span class="sxs-lookup"><span data-stu-id="c7846-211">False</span></span>                                        |
| <span data-ttu-id="c7846-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c7846-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="c7846-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c7846-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c7846-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c7846-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c7846-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c7846-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c7846-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c7846-216">Search-Flags</span></span>           | <span data-ttu-id="c7846-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c7846-217">0x00000000</span></span>                                   |
| <span data-ttu-id="c7846-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c7846-218">System-Flags</span></span>           | <span data-ttu-id="c7846-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c7846-219">0x00000010</span></span>                                   |
| <span data-ttu-id="c7846-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c7846-220">Classes used in</span></span>        | [<span data-ttu-id="c7846-221">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="c7846-221">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c7846-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c7846-222">Windows Server 2012</span></span>



| <span data-ttu-id="c7846-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="c7846-223">Entry</span></span> | <span data-ttu-id="c7846-224">Valor</span><span class="sxs-lookup"><span data-stu-id="c7846-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c7846-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="c7846-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c7846-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c7846-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c7846-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="c7846-227">System-Only</span></span>            | <span data-ttu-id="c7846-228">Falso</span><span class="sxs-lookup"><span data-stu-id="c7846-228">False</span></span>                                        |
| <span data-ttu-id="c7846-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c7846-229">Is-Single-Valued</span></span>       | <span data-ttu-id="c7846-230">True</span><span class="sxs-lookup"><span data-stu-id="c7846-230">True</span></span>                                         |
| <span data-ttu-id="c7846-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="c7846-231">Is Indexed</span></span>             | <span data-ttu-id="c7846-232">Falso</span><span class="sxs-lookup"><span data-stu-id="c7846-232">False</span></span>                                        |
| <span data-ttu-id="c7846-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c7846-233">In Global Catalog</span></span>      | <span data-ttu-id="c7846-234">Falso</span><span class="sxs-lookup"><span data-stu-id="c7846-234">False</span></span>                                        |
| <span data-ttu-id="c7846-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c7846-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="c7846-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c7846-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c7846-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c7846-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c7846-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c7846-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c7846-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c7846-239">Search-Flags</span></span>           | <span data-ttu-id="c7846-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c7846-240">0x00000000</span></span>                                   |
| <span data-ttu-id="c7846-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c7846-241">System-Flags</span></span>           | <span data-ttu-id="c7846-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c7846-242">0x00000010</span></span>                                   |
| <span data-ttu-id="c7846-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c7846-243">Classes used in</span></span>        | [<span data-ttu-id="c7846-244">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="c7846-244">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





