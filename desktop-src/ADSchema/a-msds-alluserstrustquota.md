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
# <a name="ms-ds-all-users-trust-quota-attribute"></a><span data-ttu-id="2e13a-105">Atributo MS-DS-All-Users-Trust-quota</span><span class="sxs-lookup"><span data-stu-id="2e13a-105">MS-DS-All-Users-Trust-Quota attribute</span></span>

<span data-ttu-id="2e13a-106">Usado para impor uma cota de usuários combinados no número total de objetos Trusted-Domain criados usando o direito de acesso de novo controle, criar-entrada-floresta-Trust.</span><span class="sxs-lookup"><span data-stu-id="2e13a-106">Used to enforce a combined users quota on the total number of Trusted-Domain objects created by using the new control access right, Create-Inbound-Forest-Trust.</span></span>



| <span data-ttu-id="2e13a-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="2e13a-107">Entry</span></span> | <span data-ttu-id="2e13a-108">Valor</span><span class="sxs-lookup"><span data-stu-id="2e13a-108">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="2e13a-109">CN</span><span class="sxs-lookup"><span data-stu-id="2e13a-109">CN</span></span>                | <span data-ttu-id="2e13a-110">MS-DS-All-Users-Trust-quota</span><span class="sxs-lookup"><span data-stu-id="2e13a-110">MS-DS-All-Users-Trust-Quota</span></span>               |
| <span data-ttu-id="2e13a-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2e13a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2e13a-112">msDS-AllUsersTrustQuota</span><span class="sxs-lookup"><span data-stu-id="2e13a-112">msDS-AllUsersTrustQuota</span></span>                   |
| <span data-ttu-id="2e13a-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="2e13a-113">Size</span></span>              | \-                                        |
| <span data-ttu-id="2e13a-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="2e13a-114">Update Privilege</span></span>  | <span data-ttu-id="2e13a-115">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="2e13a-115">Domain administrator</span></span>                      |
| <span data-ttu-id="2e13a-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="2e13a-116">Update Frequency</span></span>  | <span data-ttu-id="2e13a-117">Na criação da floresta e raramente depois disso.</span><span class="sxs-lookup"><span data-stu-id="2e13a-117">At forest creation and rarely after that.</span></span> |
| <span data-ttu-id="2e13a-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2e13a-118">Attribute-Id</span></span>      | <span data-ttu-id="2e13a-119">1.2.840.113556.1.4.1789</span><span class="sxs-lookup"><span data-stu-id="2e13a-119">1.2.840.113556.1.4.1789</span></span>                   |
| <span data-ttu-id="2e13a-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2e13a-120">System-Id-Guid</span></span>    | <span data-ttu-id="2e13a-121">d3aa4a5c-4e03-4810-97aa-2b339e7a434b</span><span class="sxs-lookup"><span data-stu-id="2e13a-121">d3aa4a5c-4e03-4810-97aa-2b339e7a434b</span></span>      |
| <span data-ttu-id="2e13a-122">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2e13a-122">Syntax</span></span>            | [<span data-ttu-id="2e13a-123">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="2e13a-123">**Enumeration**</span></span>](s-enumeration.md)      |



## <a name="implementations"></a><span data-ttu-id="2e13a-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="2e13a-124">Implementations</span></span>

-   [<span data-ttu-id="2e13a-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2e13a-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2e13a-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2e13a-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2e13a-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2e13a-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2e13a-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2e13a-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2e13a-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2e13a-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="2e13a-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2e13a-130">Windows Server 2003</span></span>



| <span data-ttu-id="2e13a-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="2e13a-131">Entry</span></span> | <span data-ttu-id="2e13a-132">Valor</span><span class="sxs-lookup"><span data-stu-id="2e13a-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2e13a-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="2e13a-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2e13a-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e13a-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2e13a-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e13a-135">System-Only</span></span>            | <span data-ttu-id="2e13a-136">Falso</span><span class="sxs-lookup"><span data-stu-id="2e13a-136">False</span></span>                                        |
| <span data-ttu-id="2e13a-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2e13a-137">Is-Single-Valued</span></span>       | <span data-ttu-id="2e13a-138">True</span><span class="sxs-lookup"><span data-stu-id="2e13a-138">True</span></span>                                         |
| <span data-ttu-id="2e13a-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="2e13a-139">Is Indexed</span></span>             | <span data-ttu-id="2e13a-140">Falso</span><span class="sxs-lookup"><span data-stu-id="2e13a-140">False</span></span>                                        |
| <span data-ttu-id="2e13a-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2e13a-141">In Global Catalog</span></span>      | <span data-ttu-id="2e13a-142">Falso</span><span class="sxs-lookup"><span data-stu-id="2e13a-142">False</span></span>                                        |
| <span data-ttu-id="2e13a-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2e13a-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e13a-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2e13a-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2e13a-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e13a-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2e13a-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e13a-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2e13a-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e13a-147">Search-Flags</span></span>           | <span data-ttu-id="2e13a-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e13a-148">0x00000000</span></span>                                   |
| <span data-ttu-id="2e13a-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e13a-149">System-Flags</span></span>           | <span data-ttu-id="2e13a-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e13a-150">0x00000010</span></span>                                   |
| <span data-ttu-id="2e13a-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2e13a-151">Classes used in</span></span>        | [<span data-ttu-id="2e13a-152">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="2e13a-152">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2e13a-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2e13a-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2e13a-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="2e13a-154">Entry</span></span> | <span data-ttu-id="2e13a-155">Valor</span><span class="sxs-lookup"><span data-stu-id="2e13a-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2e13a-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="2e13a-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2e13a-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e13a-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2e13a-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e13a-158">System-Only</span></span>            | <span data-ttu-id="2e13a-159">Falso</span><span class="sxs-lookup"><span data-stu-id="2e13a-159">False</span></span>                                        |
| <span data-ttu-id="2e13a-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2e13a-160">Is-Single-Valued</span></span>       | <span data-ttu-id="2e13a-161">True</span><span class="sxs-lookup"><span data-stu-id="2e13a-161">True</span></span>                                         |
| <span data-ttu-id="2e13a-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="2e13a-162">Is Indexed</span></span>             | <span data-ttu-id="2e13a-163">Falso</span><span class="sxs-lookup"><span data-stu-id="2e13a-163">False</span></span>                                        |
| <span data-ttu-id="2e13a-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2e13a-164">In Global Catalog</span></span>      | <span data-ttu-id="2e13a-165">Falso</span><span class="sxs-lookup"><span data-stu-id="2e13a-165">False</span></span>                                        |
| <span data-ttu-id="2e13a-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2e13a-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e13a-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2e13a-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2e13a-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e13a-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2e13a-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e13a-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2e13a-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e13a-170">Search-Flags</span></span>           | <span data-ttu-id="2e13a-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e13a-171">0x00000000</span></span>                                   |
| <span data-ttu-id="2e13a-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e13a-172">System-Flags</span></span>           | <span data-ttu-id="2e13a-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e13a-173">0x00000010</span></span>                                   |
| <span data-ttu-id="2e13a-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2e13a-174">Classes used in</span></span>        | [<span data-ttu-id="2e13a-175">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="2e13a-175">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2e13a-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e13a-176">Windows Server 2008</span></span>



| <span data-ttu-id="2e13a-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="2e13a-177">Entry</span></span> | <span data-ttu-id="2e13a-178">Valor</span><span class="sxs-lookup"><span data-stu-id="2e13a-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2e13a-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="2e13a-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2e13a-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e13a-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2e13a-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e13a-181">System-Only</span></span>            | <span data-ttu-id="2e13a-182">Falso</span><span class="sxs-lookup"><span data-stu-id="2e13a-182">False</span></span>                                        |
| <span data-ttu-id="2e13a-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2e13a-183">Is-Single-Valued</span></span>       | <span data-ttu-id="2e13a-184">True</span><span class="sxs-lookup"><span data-stu-id="2e13a-184">True</span></span>                                         |
| <span data-ttu-id="2e13a-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="2e13a-185">Is Indexed</span></span>             | <span data-ttu-id="2e13a-186">Falso</span><span class="sxs-lookup"><span data-stu-id="2e13a-186">False</span></span>                                        |
| <span data-ttu-id="2e13a-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2e13a-187">In Global Catalog</span></span>      | <span data-ttu-id="2e13a-188">Falso</span><span class="sxs-lookup"><span data-stu-id="2e13a-188">False</span></span>                                        |
| <span data-ttu-id="2e13a-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2e13a-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e13a-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2e13a-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2e13a-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e13a-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2e13a-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e13a-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2e13a-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e13a-193">Search-Flags</span></span>           | <span data-ttu-id="2e13a-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e13a-194">0x00000000</span></span>                                   |
| <span data-ttu-id="2e13a-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e13a-195">System-Flags</span></span>           | <span data-ttu-id="2e13a-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e13a-196">0x00000010</span></span>                                   |
| <span data-ttu-id="2e13a-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2e13a-197">Classes used in</span></span>        | [<span data-ttu-id="2e13a-198">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="2e13a-198">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2e13a-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2e13a-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2e13a-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="2e13a-200">Entry</span></span> | <span data-ttu-id="2e13a-201">Valor</span><span class="sxs-lookup"><span data-stu-id="2e13a-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2e13a-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="2e13a-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2e13a-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e13a-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2e13a-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e13a-204">System-Only</span></span>            | <span data-ttu-id="2e13a-205">Falso</span><span class="sxs-lookup"><span data-stu-id="2e13a-205">False</span></span>                                        |
| <span data-ttu-id="2e13a-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2e13a-206">Is-Single-Valued</span></span>       | <span data-ttu-id="2e13a-207">True</span><span class="sxs-lookup"><span data-stu-id="2e13a-207">True</span></span>                                         |
| <span data-ttu-id="2e13a-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="2e13a-208">Is Indexed</span></span>             | <span data-ttu-id="2e13a-209">Falso</span><span class="sxs-lookup"><span data-stu-id="2e13a-209">False</span></span>                                        |
| <span data-ttu-id="2e13a-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2e13a-210">In Global Catalog</span></span>      | <span data-ttu-id="2e13a-211">Falso</span><span class="sxs-lookup"><span data-stu-id="2e13a-211">False</span></span>                                        |
| <span data-ttu-id="2e13a-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2e13a-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e13a-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2e13a-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2e13a-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e13a-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2e13a-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e13a-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2e13a-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e13a-216">Search-Flags</span></span>           | <span data-ttu-id="2e13a-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e13a-217">0x00000000</span></span>                                   |
| <span data-ttu-id="2e13a-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e13a-218">System-Flags</span></span>           | <span data-ttu-id="2e13a-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e13a-219">0x00000010</span></span>                                   |
| <span data-ttu-id="2e13a-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2e13a-220">Classes used in</span></span>        | [<span data-ttu-id="2e13a-221">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="2e13a-221">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2e13a-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2e13a-222">Windows Server 2012</span></span>



| <span data-ttu-id="2e13a-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="2e13a-223">Entry</span></span> | <span data-ttu-id="2e13a-224">Valor</span><span class="sxs-lookup"><span data-stu-id="2e13a-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2e13a-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="2e13a-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2e13a-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e13a-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2e13a-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e13a-227">System-Only</span></span>            | <span data-ttu-id="2e13a-228">Falso</span><span class="sxs-lookup"><span data-stu-id="2e13a-228">False</span></span>                                        |
| <span data-ttu-id="2e13a-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2e13a-229">Is-Single-Valued</span></span>       | <span data-ttu-id="2e13a-230">True</span><span class="sxs-lookup"><span data-stu-id="2e13a-230">True</span></span>                                         |
| <span data-ttu-id="2e13a-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="2e13a-231">Is Indexed</span></span>             | <span data-ttu-id="2e13a-232">Falso</span><span class="sxs-lookup"><span data-stu-id="2e13a-232">False</span></span>                                        |
| <span data-ttu-id="2e13a-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2e13a-233">In Global Catalog</span></span>      | <span data-ttu-id="2e13a-234">Falso</span><span class="sxs-lookup"><span data-stu-id="2e13a-234">False</span></span>                                        |
| <span data-ttu-id="2e13a-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2e13a-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e13a-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2e13a-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2e13a-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e13a-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2e13a-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e13a-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2e13a-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e13a-239">Search-Flags</span></span>           | <span data-ttu-id="2e13a-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e13a-240">0x00000000</span></span>                                   |
| <span data-ttu-id="2e13a-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e13a-241">System-Flags</span></span>           | <span data-ttu-id="2e13a-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e13a-242">0x00000010</span></span>                                   |
| <span data-ttu-id="2e13a-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2e13a-243">Classes used in</span></span>        | [<span data-ttu-id="2e13a-244">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="2e13a-244">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





