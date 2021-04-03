---
title: Atributo MS-DS-All-Users-Trust-quota
description: Usado para impor uma cota de usuários combinados no número total de objetos Trusted-Domain criados usando o direito de acesso de novo controle, criar-entrada-floresta-Trust.
ms.assetid: 77e70a26-99b4-4b49-a984-6809d02f6fb8
ms.tgt_platform: multiple
keywords:
- MS-DS-All-Users-Trust-quota atributo AD Schema
- atributo msDS-AllUsersTrustQuota do AD Schema
topic_type:
- apiref
api_name:
- MS-DS-All-Users-Trust-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0538ff38f1eb57f339a8e0e244a378a36dd92498
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645571"
---
# <a name="ms-ds-all-users-trust-quota-attribute"></a><span data-ttu-id="e3c8d-105">Atributo MS-DS-All-Users-Trust-quota</span><span class="sxs-lookup"><span data-stu-id="e3c8d-105">MS-DS-All-Users-Trust-Quota attribute</span></span>

<span data-ttu-id="e3c8d-106">Usado para impor uma cota de usuários combinados no número total de objetos Trusted-Domain criados usando o direito de acesso de novo controle, criar-entrada-floresta-Trust.</span><span class="sxs-lookup"><span data-stu-id="e3c8d-106">Used to enforce a combined users quota on the total number of Trusted-Domain objects created by using the new control access right, Create-Inbound-Forest-Trust.</span></span>



| <span data-ttu-id="e3c8d-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="e3c8d-107">Entry</span></span> | <span data-ttu-id="e3c8d-108">Valor</span><span class="sxs-lookup"><span data-stu-id="e3c8d-108">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="e3c8d-109">CN</span><span class="sxs-lookup"><span data-stu-id="e3c8d-109">CN</span></span>                | <span data-ttu-id="e3c8d-110">MS-DS-All-Users-Trust-quota</span><span class="sxs-lookup"><span data-stu-id="e3c8d-110">MS-DS-All-Users-Trust-Quota</span></span>               |
| <span data-ttu-id="e3c8d-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e3c8d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e3c8d-112">msDS-AllUsersTrustQuota</span><span class="sxs-lookup"><span data-stu-id="e3c8d-112">msDS-AllUsersTrustQuota</span></span>                   |
| <span data-ttu-id="e3c8d-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="e3c8d-113">Size</span></span>              | \-                                        |
| <span data-ttu-id="e3c8d-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="e3c8d-114">Update Privilege</span></span>  | <span data-ttu-id="e3c8d-115">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="e3c8d-115">Domain administrator</span></span>                      |
| <span data-ttu-id="e3c8d-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="e3c8d-116">Update Frequency</span></span>  | <span data-ttu-id="e3c8d-117">Na criação da floresta e raramente depois disso.</span><span class="sxs-lookup"><span data-stu-id="e3c8d-117">At forest creation and rarely after that.</span></span> |
| <span data-ttu-id="e3c8d-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e3c8d-118">Attribute-Id</span></span>      | <span data-ttu-id="e3c8d-119">1.2.840.113556.1.4.1789</span><span class="sxs-lookup"><span data-stu-id="e3c8d-119">1.2.840.113556.1.4.1789</span></span>                   |
| <span data-ttu-id="e3c8d-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e3c8d-120">System-Id-Guid</span></span>    | <span data-ttu-id="e3c8d-121">d3aa4a5c-4e03-4810-97aa-2b339e7a434b</span><span class="sxs-lookup"><span data-stu-id="e3c8d-121">d3aa4a5c-4e03-4810-97aa-2b339e7a434b</span></span>      |
| <span data-ttu-id="e3c8d-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3c8d-122">Syntax</span></span>            | [<span data-ttu-id="e3c8d-123">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="e3c8d-123">**Enumeration**</span></span>](s-enumeration.md)      |



## <a name="implementations"></a><span data-ttu-id="e3c8d-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="e3c8d-124">Implementations</span></span>

-   [<span data-ttu-id="e3c8d-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e3c8d-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e3c8d-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e3c8d-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e3c8d-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e3c8d-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e3c8d-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e3c8d-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e3c8d-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e3c8d-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="e3c8d-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e3c8d-130">Windows Server 2003</span></span>



| <span data-ttu-id="e3c8d-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="e3c8d-131">Entry</span></span> | <span data-ttu-id="e3c8d-132">Valor</span><span class="sxs-lookup"><span data-stu-id="e3c8d-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e3c8d-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="e3c8d-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e3c8d-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3c8d-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e3c8d-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3c8d-135">System-Only</span></span>            | <span data-ttu-id="e3c8d-136">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c8d-136">False</span></span>                                        |
| <span data-ttu-id="e3c8d-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e3c8d-137">Is-Single-Valued</span></span>       | <span data-ttu-id="e3c8d-138">True</span><span class="sxs-lookup"><span data-stu-id="e3c8d-138">True</span></span>                                         |
| <span data-ttu-id="e3c8d-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="e3c8d-139">Is Indexed</span></span>             | <span data-ttu-id="e3c8d-140">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c8d-140">False</span></span>                                        |
| <span data-ttu-id="e3c8d-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e3c8d-141">In Global Catalog</span></span>      | <span data-ttu-id="e3c8d-142">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c8d-142">False</span></span>                                        |
| <span data-ttu-id="e3c8d-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e3c8d-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3c8d-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e3c8d-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e3c8d-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3c8d-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e3c8d-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3c8d-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e3c8d-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3c8d-147">Search-Flags</span></span>           | <span data-ttu-id="e3c8d-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3c8d-148">0x00000000</span></span>                                   |
| <span data-ttu-id="e3c8d-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3c8d-149">System-Flags</span></span>           | <span data-ttu-id="e3c8d-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e3c8d-150">0x00000010</span></span>                                   |
| <span data-ttu-id="e3c8d-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e3c8d-151">Classes used in</span></span>        | [<span data-ttu-id="e3c8d-152">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="e3c8d-152">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e3c8d-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e3c8d-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e3c8d-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="e3c8d-154">Entry</span></span> | <span data-ttu-id="e3c8d-155">Valor</span><span class="sxs-lookup"><span data-stu-id="e3c8d-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e3c8d-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="e3c8d-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e3c8d-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3c8d-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e3c8d-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3c8d-158">System-Only</span></span>            | <span data-ttu-id="e3c8d-159">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c8d-159">False</span></span>                                        |
| <span data-ttu-id="e3c8d-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e3c8d-160">Is-Single-Valued</span></span>       | <span data-ttu-id="e3c8d-161">True</span><span class="sxs-lookup"><span data-stu-id="e3c8d-161">True</span></span>                                         |
| <span data-ttu-id="e3c8d-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="e3c8d-162">Is Indexed</span></span>             | <span data-ttu-id="e3c8d-163">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c8d-163">False</span></span>                                        |
| <span data-ttu-id="e3c8d-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e3c8d-164">In Global Catalog</span></span>      | <span data-ttu-id="e3c8d-165">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c8d-165">False</span></span>                                        |
| <span data-ttu-id="e3c8d-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e3c8d-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3c8d-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e3c8d-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e3c8d-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3c8d-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e3c8d-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3c8d-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e3c8d-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3c8d-170">Search-Flags</span></span>           | <span data-ttu-id="e3c8d-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3c8d-171">0x00000000</span></span>                                   |
| <span data-ttu-id="e3c8d-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3c8d-172">System-Flags</span></span>           | <span data-ttu-id="e3c8d-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e3c8d-173">0x00000010</span></span>                                   |
| <span data-ttu-id="e3c8d-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e3c8d-174">Classes used in</span></span>        | [<span data-ttu-id="e3c8d-175">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="e3c8d-175">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e3c8d-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3c8d-176">Windows Server 2008</span></span>



| <span data-ttu-id="e3c8d-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="e3c8d-177">Entry</span></span> | <span data-ttu-id="e3c8d-178">Valor</span><span class="sxs-lookup"><span data-stu-id="e3c8d-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e3c8d-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="e3c8d-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e3c8d-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3c8d-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e3c8d-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3c8d-181">System-Only</span></span>            | <span data-ttu-id="e3c8d-182">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c8d-182">False</span></span>                                        |
| <span data-ttu-id="e3c8d-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e3c8d-183">Is-Single-Valued</span></span>       | <span data-ttu-id="e3c8d-184">True</span><span class="sxs-lookup"><span data-stu-id="e3c8d-184">True</span></span>                                         |
| <span data-ttu-id="e3c8d-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="e3c8d-185">Is Indexed</span></span>             | <span data-ttu-id="e3c8d-186">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c8d-186">False</span></span>                                        |
| <span data-ttu-id="e3c8d-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e3c8d-187">In Global Catalog</span></span>      | <span data-ttu-id="e3c8d-188">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c8d-188">False</span></span>                                        |
| <span data-ttu-id="e3c8d-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e3c8d-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3c8d-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e3c8d-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e3c8d-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3c8d-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e3c8d-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3c8d-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e3c8d-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3c8d-193">Search-Flags</span></span>           | <span data-ttu-id="e3c8d-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3c8d-194">0x00000000</span></span>                                   |
| <span data-ttu-id="e3c8d-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3c8d-195">System-Flags</span></span>           | <span data-ttu-id="e3c8d-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e3c8d-196">0x00000010</span></span>                                   |
| <span data-ttu-id="e3c8d-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e3c8d-197">Classes used in</span></span>        | [<span data-ttu-id="e3c8d-198">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="e3c8d-198">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e3c8d-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e3c8d-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e3c8d-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="e3c8d-200">Entry</span></span> | <span data-ttu-id="e3c8d-201">Valor</span><span class="sxs-lookup"><span data-stu-id="e3c8d-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e3c8d-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="e3c8d-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e3c8d-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3c8d-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e3c8d-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3c8d-204">System-Only</span></span>            | <span data-ttu-id="e3c8d-205">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c8d-205">False</span></span>                                        |
| <span data-ttu-id="e3c8d-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e3c8d-206">Is-Single-Valued</span></span>       | <span data-ttu-id="e3c8d-207">True</span><span class="sxs-lookup"><span data-stu-id="e3c8d-207">True</span></span>                                         |
| <span data-ttu-id="e3c8d-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="e3c8d-208">Is Indexed</span></span>             | <span data-ttu-id="e3c8d-209">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c8d-209">False</span></span>                                        |
| <span data-ttu-id="e3c8d-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e3c8d-210">In Global Catalog</span></span>      | <span data-ttu-id="e3c8d-211">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c8d-211">False</span></span>                                        |
| <span data-ttu-id="e3c8d-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e3c8d-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3c8d-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e3c8d-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e3c8d-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3c8d-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e3c8d-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3c8d-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e3c8d-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3c8d-216">Search-Flags</span></span>           | <span data-ttu-id="e3c8d-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3c8d-217">0x00000000</span></span>                                   |
| <span data-ttu-id="e3c8d-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3c8d-218">System-Flags</span></span>           | <span data-ttu-id="e3c8d-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e3c8d-219">0x00000010</span></span>                                   |
| <span data-ttu-id="e3c8d-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e3c8d-220">Classes used in</span></span>        | [<span data-ttu-id="e3c8d-221">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="e3c8d-221">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e3c8d-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e3c8d-222">Windows Server 2012</span></span>



| <span data-ttu-id="e3c8d-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="e3c8d-223">Entry</span></span> | <span data-ttu-id="e3c8d-224">Valor</span><span class="sxs-lookup"><span data-stu-id="e3c8d-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e3c8d-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="e3c8d-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e3c8d-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e3c8d-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e3c8d-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="e3c8d-227">System-Only</span></span>            | <span data-ttu-id="e3c8d-228">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c8d-228">False</span></span>                                        |
| <span data-ttu-id="e3c8d-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e3c8d-229">Is-Single-Valued</span></span>       | <span data-ttu-id="e3c8d-230">True</span><span class="sxs-lookup"><span data-stu-id="e3c8d-230">True</span></span>                                         |
| <span data-ttu-id="e3c8d-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="e3c8d-231">Is Indexed</span></span>             | <span data-ttu-id="e3c8d-232">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c8d-232">False</span></span>                                        |
| <span data-ttu-id="e3c8d-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e3c8d-233">In Global Catalog</span></span>      | <span data-ttu-id="e3c8d-234">Falso</span><span class="sxs-lookup"><span data-stu-id="e3c8d-234">False</span></span>                                        |
| <span data-ttu-id="e3c8d-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e3c8d-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="e3c8d-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e3c8d-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e3c8d-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e3c8d-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e3c8d-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e3c8d-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e3c8d-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e3c8d-239">Search-Flags</span></span>           | <span data-ttu-id="e3c8d-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3c8d-240">0x00000000</span></span>                                   |
| <span data-ttu-id="e3c8d-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e3c8d-241">System-Flags</span></span>           | <span data-ttu-id="e3c8d-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e3c8d-242">0x00000010</span></span>                                   |
| <span data-ttu-id="e3c8d-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e3c8d-243">Classes used in</span></span>        | [<span data-ttu-id="e3c8d-244">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="e3c8d-244">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





